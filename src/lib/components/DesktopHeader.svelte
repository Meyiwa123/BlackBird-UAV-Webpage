<script lang="ts">
	import { goto } from '$app/navigation';
	import Tab, { Label } from '@smui/tab';
	import TabBar from '@smui/tab-bar';
	import JoinUs from '$lib/components/JoinUs.svelte';

	let active = 'Home';

	function handleTabClick(tab: string) {
		const pageUrl = `/${tab.replace(/ /g, '_')}`;
		goto(pageUrl);
	}
</script>

<div class="tabbar-container">
	<TabBar tabs={['home', 'team', 'competition', 'sponsors', 'events']} let:tab bind:active>
		<Tab
			{tab}
			on:click={() => handleTabClick(tab)}
			target="href-tabs-frame"
			tabIndicator$type="icon"
			tabIndicator$content$class="material-icons"
		>
			<Label>{tab}</Label>
			<svelte:fragment slot="tab-indicator">star</svelte:fragment>
		</Tab>
	</TabBar>
</div>
<JoinUs />

<style>
	.tabbar-container {
		margin-left: auto;
	}
</style>
