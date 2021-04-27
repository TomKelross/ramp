<script lang="typescript">
	import StickyLabel from "./StickyLabel.svelte";

	import { onMount } from "svelte";
	import Navbar from "./components/Navbar.svelte";
	import Hero from "./components/Hero.svelte";
	import Background from "./Background.svelte";
	import WhoAmI from "./components/WhoAmI.svelte";

	let count: number = 0;
	onMount(() => {
		const interval = setInterval(() => count++, 1000);
		return () => {
			clearInterval(interval);
		};
	});
</script>

<div class="">
	<!-- <StickyLabel /> -->
	<Navbar />
	<WhoAmI />
	<Hero />
</div>
