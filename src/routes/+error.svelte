<script>
	import { page } from '$app/stores'
</script>

<div class="error">
	<img src="svg/warning.svg" alt="Warning" />
	<h1>{$page.status}: {$page.error?.message}</h1>
</div>

<style>
	.error {
		height: 100%;
		display: grid;
		place-content: center;
	}

	img {
		padding-top: 50pt;
		width: 230px;
		height: auto;
	}
</style>