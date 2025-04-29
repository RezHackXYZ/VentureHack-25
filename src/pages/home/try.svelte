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
				end: "+=400%", // This makes the scrollable area 3x the viewport height
				scrub: 1, // Smooth scrolling
				pin: true, // Pin the section during scrolling
			},
		});
	});
</script>

<div id="WhatWillHappen">
	<div>
		<h1>Here's what happened!</h1>
		<div id="scroll-section">
			<div id="items-container">
				<div class="item">
					<div class="StoryLine" id="StoryLine1">
						<div id="leftOf1" class="leftStroyline">
							<h3>
								You Just finished a project you<br /> have bean
								making for months.
								<hr class="textHr" />
							</h3>
						</div>
						<hr class="seperatorHr" />
						<div id="rightOf1" class="rightStroyline"></div>
					</div>
				</div>
				<div class="item">
					<div class="StoryLine" id="StoryLine2">
						<div id="leftOf2" class="leftStroyline"></div>
						<hr class="seperatorHr" />
						<div id="rightOf2" class="rightStroyline">
							<h3>
								You are about to push to prod!
								<hr class="textHr" />
							</h3>
						</div>
					</div>
				</div>
				<div class="item">
					<div class="StoryLine" id="StoryLine3">
						<div id="leftOf3" class="leftStroyline">
							<h3>
								But! you get a email.
								<hr class="textHr" />
							</h3>
						</div>
						<hr class="seperatorHr" />
						<div id="rightOf3" class="rightStroyline"></div>
					</div>
				</div>
				<div class="item">
					<div class="StoryLine" id="StoryLine4">
						<div id="leftOf4" class="leftStroyline"></div>
						<hr class="seperatorHr" />
						<div id="rightOf4" class="rightStroyline">
							<h3>
								Here is what it had to say!
								<hr class="textHr" />
							</h3>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	#WhatWillHappen {
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
	}

	.item {
		display: grid;
		place-items: center;
		width: fit-content;
		flex-shrink: 0;
		width: 100vw;
	}
	h3 {
		margin: 0;
		margin-top: 5px;
		color: white;
	}

	.seperatorHr {
		width: 10px;
		background-color: #00ff40;
		margin: 5px;
		border-radius: 20px;
		border: #00ff40;
	}

	.StoryLine {
		display: flex;
		font-size: 1.5rem;
		height: 50vh;
		width: 80vw;
		justify-content: space-between;
		border: 1px solid #00ff40;
		border-radius: 20px;
		padding: 10px;
	}
	.leftStroyline,
	.rightStroyline {
		width: 47%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		background-color: #202020;
	}

	.textHr {
		width: calc(100% - 20px);
		height: 2px;
		background-color: #00360e;
		margin: 10px;
		border-radius: 20px;
		border: #00360e;
	}
</style>
