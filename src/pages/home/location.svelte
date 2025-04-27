<script>
	import { onMount } from "svelte";
	import L from "leaflet";
	import "leaflet/dist/leaflet.css";

	let map;
	const delhiCoordinates = [28.6139, 77.209]; // Delhi's latitude and longitude

	onMount(() => {
		// Initialize the map
		map = L.map("map").setView(delhiCoordinates, 10);

		// Add OpenStreetMap tiles
		L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
			attribution:
				'&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors',
		}).addTo(map);

		// Delhi boundaries (approximate)
		var delhiBoundaries = [
			[28.813, 77.05], // Northwest
			[28.84, 77.2], // North
			[28.813, 77.35], // Northeast
			[28.674, 77.438], // East
			[28.53, 77.334], // Southeast
			[28.512, 77.2], // South
			[28.53, 77.066], // Southwest
			[28.674, 76.962], // West
		];

		var polygon = L.polygon(delhiBoundaries, {
			color: "green",
			fillColor: "#a3e635",
			fillOpacity: 0.3,
			weight: 3,
		}).addTo(map);
	});
</script>

<div id="root">
	<div id="left"><h1>Where</h1></div>
	<div id="right">
		<h2>Delhi, India!</h2>
		<div id="map"></div>
	</div>
</div>

<style>
	:global(.leaflet-container) {
		height: 100%;
		width: 100%;
	}

	#root {
		border: 1px solid #00ff40;
		border-radius: 20px;
		display: flex;
		width: fit-content;
	}

	h1,
	h2 {
		margin: 0;
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

	#map {
		height: 150px;
		width: 300px;
		border-radius: 20px;
		border-radius: 0 20px 20px 0;
	}

	#right {
		color: white;
		border-radius: 0 20px 20px 0;
		padding: 5px;
		align-items: center;
	}
</style>
