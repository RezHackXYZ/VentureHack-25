<script>
	import Router from "svelte-spa-router";

	import Home from "./pages/home/home.svelte";
	import parentsguide from "./pages/parents-guide/parents-guide.svelte";

	let routes = {
		"/": Home,
		"/parents-guide": parentsguide,
	};
</script>

<div id="root">
	<Router {routes} />
</div>

<style>
	:root {
		font-family: "JetBrains Mono", monospace;
		font-optical-sizing: auto;
		font-weight: 150;
		font-style: normal;
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
