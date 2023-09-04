<script lang="ts">
	import Button, { Label } from '@smui/button';
	let screenSize: number;
</script>

<svelte:window bind:innerWidth={screenSize} />

<main>
	<div>
		<h1>Nice to meet you!</h1>
		<p>
			We are BlackBird UAV, Carleton University aerial vehicle design team. We are a team of
			students dedicated to designing, building and flying drones.
		</p>
		<a href="https://discord.gg/Spw3F6krCn" target="_blank">
			<Button touch variant="raised">
				<Label>Join Our Club</Label>
			</Button>
		</a>
	</div>
	{#if screenSize > 768}
		<div class="right_side">
			<video autoplay loop muted>
				<source src="video/bbuav_2023.mp4" type="video/mp4" />
			</video>
		</div>
	{/if}
</main>

<style>
	main {
		padding-top: 20px;
		padding-bottom: 115px;
		display: flex;
		flex-direction: row;
		color: white;
		max-inline-size: 150ch;
	}

	div {
		padding: 2rem;
		flex: 1;
		/* background-color: #c9c7c7; */
	}

	.right_side {
		/* background-color: #f9f9f9; */
	}

	video {
		width: 100%;
		max-width: 750px;
		box-shadow: 0px 4px 10px #333;
	}
</style>
