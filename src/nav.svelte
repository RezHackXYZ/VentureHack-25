<script>
	import { gsap } from "gsap";

	import { ScrollToPlugin } from "gsap/ScrollToPlugin";

	gsap.registerPlugin(ScrollToPlugin);
	ScrollToPlugin.config({ autoKill: true });
</script>

<div id="root">
	<div id="left"><h1>VentureHacks'25</h1></div>
	<div id="right">
		<a
			href="#ani"
			role="button"
			onclick={(e) => {
				e.preventDefault();
				gsap.to(window, { duration: 1, scrollTo: "#ani" });
			}}
			onkeydown={(e) => {
				if (e.key === "Enter" || e.key === " ") {
					e.preventDefault();
					gsap.to(window, { duration: 1, scrollTo: "#ani" });
				}
			}}>/start</a
		>
		<a
			href="#WhatWillHappen"
			role="button"
			onclick={(e) => {
				e.preventDefault();
				gsap.to(window, { duration: 1, scrollTo: "#WhatWillHappen" });
			}}
			onkeydown={(e) => {
				if (e.key === "Enter" || e.key === " ") {
					e.preventDefault();
					gsap.to(window, {
						duration: 1,
						scrollTo: "#WhatWillHappen",
					});
				}
			}}>/What Will Happen</a
		>
	</div>
</div>

<style>
	#root {
		position: fixed;
		backdrop-filter: blur(10px);
		top: 0;
		left: 0;
		z-index: 10;
		border: 1px solid #00ff40;
		padding: 5px;
		margin: 20px;
		border-radius: 20px;
		width: calc(100% - 40px);
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	h1 {
		color: white;
		margin: 0px;
		text-shadow: 1px 1px 20px #00ff40;
	}

	a {
		color: white;
		text-decoration: #00ff40 underline;
		font-size: 1rem;
	}
</style>
