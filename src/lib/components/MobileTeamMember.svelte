<!-- MobileTeamMember.svelte -->
<script lang="ts">
	import List, { Item, Graphic, Text } from '@smui/list';

	export let teamMembers: string;
</script>

<div>
	<List class="demo-list" twoLine avatarList singleSelection>
		{#each teamMembers as item}
			<Item>
				<Graphic
					style="background-image: url(https://placehold.co/40x40?text={item.name
						.split(' ')
						.map((val) => val.substring(0, 1))
						.join('')});"
				/>
				<Text>
					<p>{item.name}</p>
					<p>{item.role}</p>
				</Text>
			</Item>
		{/each}
	</List>
</div>

<style>
	p {
		margin: 0;
		font-size: 15px;
		text-align: left;
	}
</style>