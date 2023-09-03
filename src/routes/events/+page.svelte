<script lang="ts">
	import { formatDate } from '$lib/utils.js';
	import events from '$lib/json/events.json';
	import Button, { Label } from '@smui/button';

	let pastEvents = events;
</script>

<main>
	<h1>Upcoming Events</h1>
	<p>
		Check our Discord and Instagram for future events! Don't hesitate to ask a question on Discord,
		or slide into our DMs on Instagram! You can check out some of our past years’ events, and stay
		stoked - we have lots of great events in the works!
	</p>
	<h1>Past Events</h1>

	<section>
		<ul class="events">
			{#each pastEvents as event}
				<li class="event">
					<div class="event-content">
						{#if event.image}
							<div>
								<img src={event.image} alt={event.title} />
							</div>
						{/if}
						<div class="event-info">
							<p class="title">{event.title}</p>
							<p class="date">{formatDate(event.date)}</p>
							<p class="description">{event.description}</p>
							{#if event.link}
								<a href={event.link} target="_blank">
									<Button variant="raised" class="button-shaped-round" style="text-align: center;">
										<Label>Read the Article</Label>
									</Button>
								</a>
							{/if}
						</div>
					</div>
				</li>
			{/each}
		</ul>
	</section>
</main>

<style>
	h1 {
		font-size: 49px;
	}

	main {
		max-inline-size: 90ch;
	}

	.events {
		display: grid;
		gap: 2rem;
		list-style: none;
	}

	.event {
		display: flex;
		align-items: center;
		margin-bottom: 30px;
	}

	.event-content {
		flex: 1;
	}

	.event:not(:last-child) {
		border-bottom: 2px solid;
		padding-bottom: 2rem;
	}

	.title {
		font-size: 18pt;
		font-weight: bold;
		text-transform: capitalize;
	}

	img {
		display: flex;
		align-items: center;
		justify-content: center;
		max-width: 50%;
		height: auto;
		border-radius: 10px;
	}
</style>
