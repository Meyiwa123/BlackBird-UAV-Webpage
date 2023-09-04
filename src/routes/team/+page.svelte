<script lang="ts">
	import TeamMember from '$lib/components/TeamMember.svelte';
	import MobileTeamMember from '$lib/components/MobileTeamMember.svelte';
	import members from '$lib/json/members.json';

	let teamMembers = members.sort((a, b) => a.name.localeCompare(b.name));
	let screenSize: number;
</script>

<svelte:window bind:innerWidth={screenSize} />

<article>
	<h1>About Us</h1>
	<div class="section">
		<div class="content">
			<p>
				Founded by two of Professor Jeremy Laliberté’s graduate students in 2009, Blackbird UAV has
				become a symbol of innovation and growth at Carleton University. From its humble beginnings,
				our club has evolved into a thriving hub of expertise and passion, attracting students from
				various disciplines, including engineering, science, undergraduates, and graduates.
			</p>
		</div>
		<div class="image">
			<img src="images/old-team.jpg" alt="old-team" />
		</div>
	</div>

	<div class="section">
		<div class="image">
			<img src="images/team.jpg" alt="team" />
		</div>
		<div class="content">
			<p>
				What sets Blackbird UAV apart is the diversity of talents and perspectives within our
				community. We believe that innovation flourishes in a collaborative environment where
				different backgrounds and skills come together. It’s this rich tapestry of experiences that
				fuels our ability to take on a wide range of challenges.
			</p>
		</div>
	</div>

	<div class="section">
		<div class="content">
			<p>
				At Blackbird UAV, we don’t shy away from complex problems; we embrace them. Our club has a
				track record of tackling cutting-edge aerial solutions and addressing real-world issues such
				as forest fire detection and crop health monitoring. With each mission, we adapt and expand
				our skills, pushing the boundaries of what is possible in the world of unmanned aerial
				vehicles.
			</p>
		</div>
		<div class="image">
			<img src="images/preparation.jpg" alt="team" />
		</div>
	</div>
	<h1>Meet Our Team</h1>
	{#if screenSize < 768}
		<MobileTeamMember {teamMembers} />
	{:else}
		<div class="container">
			<div class="grid">
				{#each teamMembers as member}
					<div class="cell">
						<TeamMember {member} />
					</div>
				{/each}
			</div>
		</div>
	{/if}

	<br /><br />
</article>

<style>
	h1 {
		font-size: 49px;
	}

	article {
		max-inline-size: 120ch;
		text-align: center;
	}

	img {
		width: 80%;
		height: auto;
		border-radius: 10px;
	}
	.section {
		display: flex;
		align-items: center;
		margin-bottom: 30px;
	}

	.content {
		flex: 1;
		max-inline-size: 60ch;
	}

	.image {
		flex: 1;
	}

	.container {
		display: flex;
		justify-content: center;
	}

	.grid {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 50px;
	}

	.cell {
		height: auto;
	}
</style>
