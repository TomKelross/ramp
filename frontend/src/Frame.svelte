<script>
    import { map } from "leaflet";
    import type { Nextbike } from "./apiTypes";
    import App from "./App.svelte";

    const delay = (millis: number) =>
        new Promise<void>((resolve, reject) => {
            setTimeout((_) => resolve(), millis);
        });

    async function getMap(): Promise<Nextbike> {
        const response: Response = await fetch("http://localhost:8000/map");
        // await delay(500000);
        if (response.ok == false) {
            throw new Error(await response.json());
        } else {
            return await response.json();
        }
    }

    let mapPromise = getMap();
</script>

{#await mapPromise}
    <div class="grid w-screen h-screen bg-red-600 place-items-center">
        <div class="spinner">
            <div class="rect1" />
            <div class="rect2" />
            <div class="rect3" />
            <div class="rect4" />
            <div class="rect5" />
        </div>
    </div>
{:then map}
    <App {map} />
{:catch error}
    <h1>Could not load map</h1>
{/await}

<!-- markup (zero or more items) goes here -->
<style>
    /* your styles go here */
    .spinner {
        margin: 100px auto;
        width: 50px;
        height: 40px;
        text-align: center;
        font-size: 10px;
    }

    .spinner > div {
        background-color: #333;
        height: 100%;
        width: 6px;
        display: inline-block;

        -webkit-animation: sk-stretchdelay 1.2s infinite ease-in-out;
        animation: sk-stretchdelay 1.2s infinite ease-in-out;
    }

    .spinner .rect2 {
        -webkit-animation-delay: -1.1s;
        animation-delay: -1.1s;
    }

    .spinner .rect3 {
        -webkit-animation-delay: -1s;
        animation-delay: -1s;
    }

    .spinner .rect4 {
        -webkit-animation-delay: -0.9s;
        animation-delay: -0.9s;
    }

    .spinner .rect5 {
        -webkit-animation-delay: -0.8s;
        animation-delay: -0.8s;
    }

    @-webkit-keyframes sk-stretchdelay {
        0%,
        40%,
        100% {
            -webkit-transform: scaleY(0.4);
        }
        20% {
            -webkit-transform: scaleY(1);
        }
    }

    @keyframes sk-stretchdelay {
        0%,
        40%,
        100% {
            transform: scaleY(0.4);
            -webkit-transform: scaleY(0.4);
        }
        20% {
            transform: scaleY(1);
            -webkit-transform: scaleY(1);
        }
    }
</style>
