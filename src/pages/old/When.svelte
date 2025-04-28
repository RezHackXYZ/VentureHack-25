<div id="root">
	<div id="left"><h1>Timings</h1></div>
	<div id="right">
		<div>
			<p>When</p>
			<h2>Summer 2025</h2>
			<p>How Long</p>
			<h2>48 Hours!</h2>
		</div>
	</div>
</div>

<style>
	#root {
		border: 1px solid #00ff40;
		border-radius: 20px;
		display: flex;
		width: fit-content;
	}

	h1,
	h2,
	p {
		margin: 0;
	}

	h2 {
		margin-bottom: 10px;
	}

	#left {
		background-color: #00ff40;
		color: black;
		border-radius: 20px 0 0 20px;
		padding-left: 10px;
		padding-right: 10px;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	#right {
		color: white;
		border-radius: 0 20px 20px 0;
		padding: 5px;
		display: grid;
		place-items: center;
        padding-right: 20px;
        padding-left: 20px;
	}
</style>
