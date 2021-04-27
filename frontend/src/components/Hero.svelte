<script>
    import MapSvg from "./MapSVG.svelte";
</script>

<section
    class="m-8 text-gray-600 bg-white border-8 border-t-8 body-font border-sblue"
>
    <div class="text-5xl text-white bg-sblue font-khand p2-3">Introduction</div>
    <div
        class="container flex flex-col items-center justify-center px-5 py-24 mx-auto"
    >
        <div class="w-2/6 h-2/6">
            <MapSvg />
        </div>
        <div class="w-full pt-3 text-center lg:w-2/4">
            <h1
                class="mb-4 text-4xl font-medium sm:text-6xl text-sblue font-khand title-font sm:text-4xl "
            >
                Realtime Accessibility Mapping Project
            </h1>
            <p class="mb-8 leading-relaxed">You</p>

            <hr class="pt-2" />
            <h1 class="pb-4 text-4xl font-abel text-slight">Learn more.</h1>
            <div class="flex justify-center">
                <button
                    class="inline-flex px-6 py-2 text-lg text-white bg-indigo-500 border-0 rounded focus:outline-none hover:bg-indigo-600"
                    >Learn More</button
                >
            </div>
        </div>
    </div>
</section>
