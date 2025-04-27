<script>
	import Ani from "./ani.svelte";
	import Moreinfo from "./moreinfo.svelte";
</script>

<div id="root">
	<Ani />

	<div id="content">
		<Moreinfo />
	</div>
</div>

<style>
	#root {
		position: relative;
		width: 100%;
	}

	#content {
		position: relative;
		z-index: 1;
		background-color: #2b2b2b;
		min-height: 100vh;
		color: #ffffff;
	}
</style>
