<script>
	import { gsap } from "gsap";
	import { ScrollTrigger } from "gsap/ScrollTrigger";
	import { onMount } from "svelte";

	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		const textTimeline = gsap.timeline({
			scrollTrigger: {
				trigger: "#ani",
				start: "top top",
				end: "+=300%",
				pin: true,
				scrub: 1,
				markers: false,
			},
		});

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
			)
			.to(
				".FrontText:nth-child(6)",
				{ opacity: 1, y: 0, duration: 1 },
				"-=0.5"
			);
	});
</script>

<div id="ani">
	<h4 class="FrontText">Join us this Summer 2025</h4>
	<h3 class="FrontText">Along with 100+ Teen Hackers In Delhi, India</h3>
	<h2 class="FrontText">Where We will make awsome stuff</h2>
	<h2 class="FrontText">And win awsome prizes</h2>
	<h1 class="FrontText">VentureHack'25</h1>
	<button id="RSVPFrontTextButton" class="FrontText">RSVP NOW</button>
</div>

<div id="scroolBadge">
	Scroll Down To continue<svg
		xmlns="http://www.w3.org/2000/svg"
		height="24px"
		viewBox="0 -960 960 960"
		width="24px"
		fill="#FFFFFF"
		><path
			d="M180-360 40-500l42-42 70 70q-6-27-9-54t-3-54q0-82 27-159t78-141l43 43q-43 56-65.5 121.5T200-580q0 26 3 51.5t10 50.5l65-64 42 42-140 140Zm478 233q-23 8-46.5 7.5T566-131L304-253l18-40q10-20 28-32.5t40-14.5l68-5-112-307q-6-16 1-30.5t23-20.5q16-6 30.5 1t20.5 23l148 407-100 7 131 61q7 3 15 3.5t15-1.5l157-57q31-11 45-41.5t3-61.5l-55-150q-6-16 1-30.5t23-20.5q16-6 30.5 1t20.5 23l55 150q23 63-4.5 122.5T815-184l-157 57Zm-90-265-54-151q-6-16 1-30.5t23-20.5q16-6 30.5 1t20.5 23l55 150-76 28Zm113-41-41-113q-6-16 1-30.5t23-20.5q16-6 30.5 1t20.5 23l41 112-75 28Zm8 78Z"
		/></svg
	>
</div>

<style>
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
		border: none;
		padding: 10px 20px;
		font-size: 1.5rem;
		cursor: pointer;
		border-radius: 5px;
		transition: all 0.3s ease;
		animation: bobbing 2s ease-in-out infinite;
		color: white;
	}

	#RSVPFrontTextButton:hover {
		background-color: #0056b3;
		transform: scale(1.05) rotate(2deg);
	}

	@keyframes bobbing {
		0%,
		100% {
			transform: translateY(0);
		}
		50% {
			transform: translateY(-10px);
		}
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
		display: flex;
		align-items: center;
		gap: 2px;
	}

	.FrontText {
		text-align: center;
		margin: 0;
		opacity: 0;
		transform: translateY(40px);
		will-change: opacity, transform;
	}

	.FrontText:nth-child(1) {
		color: rgb(87, 87, 87);
	}
	.FrontText:nth-child(2) {
		color: #6e6e6e;
	}
	.FrontText:nth-child(3) {
		color: #8a8a8a;
	}
	.FrontText:nth-child(4) {
		color: #8a8a8a;
	}
	.FrontText:nth-child(5) {
		color: #ffffff;
	}

	.FrontText:nth-child(1) {
		font-size: 2rem;
	}
	.FrontText:nth-child(2) {
		font-size: 3rem;
	}
	.FrontText:nth-child(3) {
		font-size: 3rem;
	}
	.FrontText:nth-child(4) {
		font-size: 4rem;
	}
	.FrontText:nth-child(5) {
		font-size: 8rem;
	}
</style>
