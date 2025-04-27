<script>
	import Staff from "./staff.svelte";
</script>

<div id="root">
	<h1>VentureHack'25</h1>

	<h2>Some Quick Insights:</h2>
	<div id="QuickInsigits">
		<p>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				height="24px"
				viewBox="0 -960 960 960"
				width="24px"
				fill="#7a7a7a"
				><path
					d="M480-480q33 0 56.5-23.5T560-560q0-33-23.5-56.5T480-640q-33 0-56.5 23.5T400-560q0 33 23.5 56.5T480-480Zm0 294q122-112 181-203.5T720-552q0-109-69.5-178.5T480-800q-101 0-170.5 69.5T240-552q0 71 59 162.5T480-186Zm0 106Q319-217 239.5-334.5T160-552q0-150 96.5-239T480-880q127 0 223.5 89T800-552q0 100-79.5 217.5T480-80Zm0-480Z"
				/></svg
			> Delhi, India
		</p>
		<p>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				height="24px"
				viewBox="0 -960 960 960"
				width="24px"
				fill="#7a7a7a"
				><path
					d="m612-292 56-56-148-148v-184h-80v216l172 172ZM480-80q-83 0-156-31.5T197-197q-54-54-85.5-127T80-480q0-83 31.5-156T197-763q54-54 127-85.5T480-880q83 0 156 31.5T763-763q54 54 85.5 127T880-480q0 83-31.5 156T763-197q-54 54-127 85.5T480-80Zm0-400Zm0 320q133 0 226.5-93.5T800-480q0-133-93.5-226.5T480-800q-133 0-226.5 93.5T160-480q0 133 93.5 226.5T480-160Z"
				/></svg
			> 48 hours
		</p>
		<p>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				height="24px"
				viewBox="0 -960 960 960"
				width="24px"
				fill="#7a7a7a"
				><path
					d="M40-160v-112q0-34 17.5-62.5T104-378q62-31 126-46.5T360-440q66 0 130 15.5T616-378q29 15 46.5 43.5T680-272v112H40Zm720 0v-120q0-44-24.5-84.5T666-434q51 6 96 20.5t84 35.5q36 20 55 44.5t19 53.5v120H760ZM360-480q-66 0-113-47t-47-113q0-66 47-113t113-47q66 0 113 47t47 113q0 66-47 113t-113 47Zm400-160q0 66-47 113t-113 47q-11 0-28-2.5t-28-5.5q27-32 41.5-71t14.5-81q0-42-14.5-81T544-792q14-5 28-6.5t28-1.5q66 0 113 47t47 113ZM120-240h480v-32q0-11-5.5-20T580-306q-54-27-109-40.5T360-360q-56 0-111 13.5T140-306q-9 5-14.5 14t-5.5 20v32Zm240-320q33 0 56.5-23.5T440-640q0-33-23.5-56.5T360-720q-33 0-56.5 23.5T280-640q0 33 23.5 56.5T360-560Zm0 320Zm0-400Z"
				/></svg
			> 100+ Teen Hackers
		</p>
		<p>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				height="24px"
				viewBox="0 -960 960 960"
				width="24px"
				fill="#7a7a7a"
				><path
					d="M200-80q-33 0-56.5-23.5T120-160v-560q0-33 23.5-56.5T200-800h40v-80h80v80h320v-80h80v80h40q33 0 56.5 23.5T840-720v560q0 33-23.5 56.5T760-80H200Zm0-80h560v-400H200v400Zm0-480h560v-80H200v80Zm0 0v-80 80Zm280 240q-17 0-28.5-11.5T440-440q0-17 11.5-28.5T480-480q17 0 28.5 11.5T520-440q0 17-11.5 28.5T480-400Zm-160 0q-17 0-28.5-11.5T280-440q0-17 11.5-28.5T320-480q17 0 28.5 11.5T360-440q0 17-11.5 28.5T320-400Zm320 0q-17 0-28.5-11.5T600-440q0-17 11.5-28.5T640-480q17 0 28.5 11.5T680-440q0 17-11.5 28.5T640-400ZM480-240q-17 0-28.5-11.5T440-280q0-17 11.5-28.5T480-320q17 0 28.5 11.5T520-280q0 17-11.5 28.5T480-240Zm-160 0q-17 0-28.5-11.5T280-280q0-17 11.5-28.5T320-320q17 0 28.5 11.5T360-280q0 17-11.5 28.5T320-240Zm320 0q-17 0-28.5-11.5T600-280q0-17 11.5-28.5T640-320q17 0 28.5 11.5T680-280q0 17-11.5 28.5T640-240Z"
				/></svg
			> Summer 2025
		</p>
	</div>
	<h2>Organizers And Volunteers:</h2>
	<div id="staff">
		<Staff
			Name="CylopsDev"
			Img="https://ca.slack-edge.com/T0266FRGM-U08BZEY0HJ9-892015462c87-512"
			Role="Organizer"
			Website="na"
			Github="na"
			Slack="https://hackclub.slack.com/team/U08BZEY0HJ9"
		/>
		<Staff
			Name="RezHackXYZ"
			Img="http://github.com/RezHackXYZ.png"
			Role="Organizer"
			Website="https://rezhack.xyz"
			Github="http://github.com/RezHackXYZ"
			Slack="https://hackclub.slack.com/team/U082KMLM7DW"
		/>
	</div>
	<h2>Sponsors:</h2>
	<div id="sponsors">
		<p>😔 None Yet! 😔</p><br>
		<button>💖 Become a Sponser! 💖</button>
	</div>
</div>

<style>
	#root {
		padding: 20px;
		align-items: center;
		text-align: center;
	}
	h1 {
		font-size: 3rem;
		margin: 0;
	}
	#QuickInsigits {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 10px;
		margin-top: 20px;
	}
	p {
		display: inline-flex;
		align-items: center;
		margin: 0;
		gap: 5px;
		color: #7a7a7a;
	}
	#staff {
		display: flex;
		justify-content: center;
		flex-direction: row;
		gap: 20px;
	}

	#sponsors > button {
        background-color: #007bff;
        border: none;
        padding: 5px;
        margin-top: 5px;
        font-size: 1rem;
        cursor: pointer;
        border-radius: 5px;
        transition: all 0.3s ease;
        color: #000;
	}
</style>
