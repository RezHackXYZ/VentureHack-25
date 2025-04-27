<script>
	import { gsap } from "gsap";
	import { ScrollTrigger } from "gsap/ScrollTrigger";
	import { onMount } from "svelte";

	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		// Create a timeline for the text reveal animations
		const textTimeline = gsap.timeline({
			scrollTrigger: {
				trigger: "#ani",
				start: "top top",
				end: "+=300%", // Adjust this to control how long the animation pins
				pin: true,
				scrub: 1,
				markers: false, // Set to true during development to see markers
			},
		});

		// Animate each text element with staggered effect
		textTimeline
			.to(".FrontText:nth-child(1)", { opacity: 1, y: 0, duration: 1 })
			.to(
				".FrontText:nth-child(2)",
				{ opacity: 1, y: 0, duration: 1 },
				"-=0.5"
			)
			.to(
				".FrontText:nth-child(3)",
				{ opacity: 1, y: 0, duration: 1 },
				"-=0.5"
			)
			.to(
				".FrontText:nth-child(4)",
				{ opacity: 1, y: 0, duration: 1 },
				"-=0.5"
			)
			.to(
				".FrontText:nth-child(5)",
				{ opacity: 1, y: 0, duration: 1 },
				"-=0.5"
			);
	});
</script>

<div id="root">
	<div id="ani">
		<h4 class="FrontText">One Idea</h4>
		<h3 class="FrontText">100+ Teen Hackers</h3>
		<h2 class="FrontText">One Hackathon This Summer</h2>
		<h1 class="FrontText">VentureHack'25</h1>
		<button id="RSVPFrontTextButton" class="FrontText">RSVP NOW</button>
	</div>

	<div id="content">
		<h2>About VentureHack'25</h2>
		<p>More information about the hackathon goes here...</p>
	</div>
	<div id=scroolBadge>Scrool Down To continue</div>
</div>

<style>
	#root {
		position: relative;
		width: 100%;
	}

	#ani {
		height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 1rem;
	}

	#RSVPFrontTextButton {
		background-color: #007bff;
		color: white;
		border: none;
		padding: 10px 20px;
		font-size: 1.5rem;
		cursor: pointer;
		border-radius: 5px;
		transition: all 0.3s ease;
	}

	#RSVPFrontTextButton:hover {
		background-color: #0056b3;
		transform: scale(1.05);
	}

	#scroolBadge {
		position: fixed;
		bottom: 20px;
		left: 50%;
		transform: translateX(-50%);
		background-color: #161616;
		color: white;
		padding: 10px 20px;
		border-radius: 100px;
		font-size: 1.2rem;
		opacity: 0.8;
	}

	#content {
		position: relative;
		z-index: 1;
		background-color: #ffffff;
		min-height: 100vh;
		padding: 2rem;
		color: #000;
	}

	.FrontText {
		text-align: center;
		margin: 0;
		opacity: 0;
		transform: translateY(40px);
		will-change: opacity, transform;
	}

	.FrontText:nth-child(1) {
		font-size: 1.5rem;
	}
	.FrontText:nth-child(2) {
		font-size: 2rem;
	}
	.FrontText:nth-child(3) {
		font-size: 3rem;
	}
	.FrontText:nth-child(4) {
		font-size: 6rem;
	}
</style>
