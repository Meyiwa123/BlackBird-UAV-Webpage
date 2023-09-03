<script lang="ts">
	import Header from './header.svelte';
	import Footer from './footer.svelte';
</script>

<div class="layout">
	<!-- Header -->
	<Header />

	<main>
		<slot />
	</main>

	<!-- Footer -->
	<Footer />
</div>

<style>
	.layout {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
</style>
