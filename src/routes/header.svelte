<script lang="ts">
	import DesktopHeader from '$lib/components/DesktopHeader.svelte';
	import MobileHeader from '$lib/components/MobileHeader.svelte';

	let screenSize: number;
</script>

<svelte:window bind:innerWidth={screenSize} />

<header>
	<div class="icon-indicators">
		<div class="flex-container">
			<img src="svg/bbuav.svg" alt="BlackBird UAV Logo" />
			{#if screenSize < 1000}
				<MobileHeader />
			{:else}
				<DesktopHeader />
			{/if}
		</div>
	</div>
</header>

<style>
	header {
		border-radius: 0 0 10px 10px;
		background-color: white;
		width: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.icon-indicators {
		display: flex;
		align-items: center;
	}

	.flex-container {
		display: flex;
		align-items: center;
	}

	img {
		width: 210px;
		height: auto;
	}

	.icon-indicators :global(.mdc-tab-indicator--active .mdc-tab-indicator__content) {
		opacity: 0.2;
	}
</style>
