<script>
	import Nav from "./nav.svelte";

	import Router from "svelte-spa-router";

	import Home from "./pages/home/home.svelte";
	import parentsguide from "./pages/parents-guide/parents-guide.svelte";

	let routes = {
		"/": Home,
		"/parents-guide": parentsguide,
	};
</script>

<!--<Nav />-->

<div id="root">
	<Router {routes} />
</div>

<style>
	:root {
		font-family: "Space Grotesk", sans-serif;
		background-color: black;
		color: white;
	}

	#root {
		height: 100%;
		display: flex;
		flex-direction: column;
		margin: 0;
	}
</style>
