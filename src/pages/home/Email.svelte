<script>
	import { gsap } from "gsap";
	import { ScrollTrigger } from "gsap/ScrollTrigger";
	import { onMount } from "svelte";

	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		const textTimeline = gsap.timeline({
			scrollTrigger: {
				trigger: "#title",
				start: "top 30%",
				end: "+=50%",
				pin: true,
				scrub: 1,
				markers: false,
			},
		});

		textTimeline.to("#title > span", {
			opacity: 1,
			y: 0,
			duration: 1,
			stagger: 0.1,
		});
	});
</script>

<div id="root">
	<h1 id="title">
		<span>V</span><span>e</span><span>n</span><span>t</span><span>u</span
		><span>r</span><span>e</span><span>H</span><span>a</span><span>c</span
		><span>k</span><span>'</span><span>2</span><span>5</span>
	</h1>
</div>

<style>
	#root {
		background-color: #444;
		padding: 20px;
		min-height: 1000vh;
	}

	#title > span {
		color: white;
		opacity: 0;
		transform: translateY(100px);
	}
</style>
