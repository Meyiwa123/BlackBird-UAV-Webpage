<script lang="ts">
	import Dialog, { Header, Title, Content } from '@smui/dialog';
	import IconButton from '@smui/icon-button';
	import Button, { Label } from '@smui/button';

	let open = false;
</script>

<Button on:click={() => (open = true)} variant="raised" class="button-shaped-round">
	<Label>Join Us</Label>
</Button>

<Dialog
	bind:open
	fullscreen
	aria-labelledby="large-scroll-title"
	aria-describedby="large-scroll-content"
	surface$style="width: 850px; max-width: calc(100vw - 32px);"
>
	<Header>
		<Title id="fullscreen-title">JOIN US IN SHAPING THE FUTURE OF FLIGHT</Title>
		<IconButton action="close" class="material-icons">close</IconButton>
	</Header>
	<Content id="fullscreen-content">
		<p>
			Are you ready to take flight with the Blackbird UAV Club at Carleton University? Join our
			passionate community of drone enthusiasts and become part of our dynamic team. Explore the
			different sub-teams within our club and discover where your skills and interests align:
		</p>
		<h1>SUBTEAMS DESCRIPTION</h1>
		<ul class="sub-teams">
			<li class="sub-team">
				<h3>Admin Team: Keeping Things in Order</h3>
				<p>
					Our Admin Team is the backbone of Blackbird UAV. We handle the logistical aspects of our
					operations, ensuring smooth coordination between subteams and club activities. If you have
					organizational skills and enjoy managing behind-the-scenes tasks, this team is perfect for
					you.
				</p>
			</li>
			<li class="sub-team">
				<h3>Mechanical Team: Crafting the Future of Drones</h3>
				<p>
					The Mechanical Team is all about designing and building the physical components of our
					drones. From airframes to propulsion systems, we create the structures that make our
					drones soar. If you’re interested in mechanical design, fabrication, and hands-on work,
					this subteam is an excellent fit.
				</p>
			</li>
			<li class="sub-team">
				<h3>Software Team: Powering Innovation with Code</h3>
				<p>
					The Software Team is responsible for the brains of our drones. We develop the software
					that controls our UAVs, enabling them to perform various tasks autonomously. If you have a
					passion for coding, algorithms, and software development, this subteam offers exciting
					opportunities.
				</p>
			</li>
		</ul>
		<h1>READY TO JOIN US?</h1>
		<p>
			To become a member of Blackbird UAV Club and be a part of our exciting journey, simply click
			the link below. We look forward to welcoming you to our club and working together to push the
			boundaries of drone technology!
		</p>
		<a href="https://discord.gg/Spw3F6krCn" target="_blank">
			<Button variant="raised" class="button-shaped-round">
				<Label>Join Our Club</Label>
			</Button>
		</a>
	</Content>
</Dialog>

<style>
	.sub-teams {
		list-style-type: none; /* Remove default list bullets */
		padding: 0;
		margin: 0;
	}

	.sub-team {
		border-left: 2px solid #333; /* Add a vertical line separator */
		padding-left: 20px; /* Adjust padding for spacing */
		margin-bottom: 20px; /* Add margin between sub-teams */
	}

	/* Additional styling for headers and content */
	h1 {
		font-size: 20px;
		text-align: center;
		color: black;
	}

	h3 {
		color: black;
	}

	p {
		font-size: 16px;
		color: black;
	}
</style>
