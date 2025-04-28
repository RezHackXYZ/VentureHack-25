<script>
	import { animate, scroll } from "motion";
	import { onMount } from "svelte";
</script>

<div id="root">
	<div>
		<div id="text">
			<h1>Here's what happened!</h1>
		</div>

		<div id="story">
			<div class="StoryLine" id="StoryLine1">
				<div id="leftOf1" class="leftStroyline">
					<h3>
						You Just finished a project you<br> have bean making for months.
						<hr class="textHr" />
					</h3>
				</div>
				<hr class="seperatorHr" />
				<div id="rightOf1" class="rightStroyline"></div>
			</div>
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
	</div>
</div>

<style>
	#root {
		display: grid;
		place-items: center;
		height: 100%;
		overflow: auto;
	}

	#story {
		width: 80vw;
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
		margin: 10px;
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
		width: 100%;
		height: 2px;
		background-color: #00360e;
		margin: 10px;
		border-radius: 20px;
		border: #00360e;
	}
	h1 {
		text-shadow: 2px 2px 30px #00ff40;
		font-size: 3rem;
		text-align: center;
	}
</style>
