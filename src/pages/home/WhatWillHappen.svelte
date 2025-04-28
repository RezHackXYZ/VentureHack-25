<script>
	import { onMount } from "svelte";
	import gsap from "gsap";
	import { ScrollTrigger } from "gsap/ScrollTrigger";

	onMount(() => {
		// Register the ScrollTrigger plugin
		gsap.registerPlugin(ScrollTrigger);

		// Create the horizontal scroll animation
		gsap.to("#items-container", {
			x: () =>
				-(
					document.querySelector("#items-container").scrollWidth -
					document.documentElement.clientWidth +
					140
				) + "px",
			ease: "none",
			scrollTrigger: {
				trigger: "#WhatWillHappen",
				start: "top top",
				// Increase this value to slow down horizontal scrolling
				end: "+=200%", // This makes the scrollable area 3x the viewport height
				scrub: 1, // Smooth scrolling
				pin: true, // Pin the section during scrolling
				anticipatePin: 1,
			},
		});
	});
</script>

<div id="WhatWillHappen">
	<div>
		<h1>What Will Happen?</h1>
		<div id="scroll-section">
			<div id="items-container">
				<div class="item">
					<span>1</span>
					<h3>Come To The Venue!</h3>
				</div>
				<div class="item">
					<span>2</span>
					<h3>Get/meet some teammates!</h3>
				</div>
				<div class="item">
					<span>3</span>
					<h3>Brainstorm what to make on the theme!</h3>
				</div>
				<div class="item">
					<span>4</span>
					<h3>Start Coding/Hacking!</h3>
				</div>
				<div class="item">
					<span>5</span>
					<h3>
						Polish, fix bugs, and give the final touches to your
						project!
					</h3>
				</div>
				<div class="item">
					<span>6</span>
					<h3>Vote for the best project!</h3>
				</div>
				<div class="item">
					<span>7</span>
					<h3>Get awesome prizes!</h3>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	#WhatWillHappen {
		background-color: #2b2b2b;
		min-height: 100vh;
		color: #ffffff;
		text-align: center;
		display: grid;
		place-items: center;
		overflow-x: hidden;
	}
	h1 {
		font-size: 3rem;
		text-shadow: 2px 2px 15px #00ff40;
	}
	#scroll-section {
		width: 100%;
		overflow: hidden;
		position: relative;
	}

	#items-container {
		display: flex;
		gap: 100px;
	}

	.item {
		display: flex;
		flex-direction: column;
		text-align: center;
		border-radius: 10px;
		padding: 10px;
		border: 1px solid #00ff40;
		width: fit-content;
		flex-shrink: 0;
		margin-right: 30px;
		margin-left: 30px;
	}

	span {
		font-size: 2em;
		font-weight: bold;
		color: #00ff40;
		margin: 0;
		height: 40px;
		width: 40px;
		background-color: #575757;
		border-radius: 10px;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	h3 {
		margin: 0;
		margin-top: 5px;
		color: white;
	}
</style>
