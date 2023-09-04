<script>
	import Button from '@smui/button';
	import JoinUs from '$lib/components/JoinUs.svelte';
</script>

<header>
	<div class="dropdown">
		<Button touch variant="raised">
			&#9776;
		</Button>
		<div class="dropdown-content">
			<a href="/home">Home</a>
			<a href="/team">Team</a>
			<a href="/competition">Competition</a>
			<a href="/sponsors">Sponsors</a>
			<a href="/events">Events</a>
			<JoinUs />
		</div>
	</div>
</header>

<style>
	/* CSS for the dropdown menu */
	.dropdown {
		position: relative;
		display: inline-block;
	}

	.dropdown-content {
		display: none;
		position: absolute;
		background-color: #f9f9f9;
		min-width: 160px;
		text-align: center;
		box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
		z-index: 1;
		border-radius: 10px 10px 10px 10px;
	}

	.dropdown-content a {
		padding: 12px 16px;
		text-decoration: none;
		display: block;
		color: #333;
	}

	.dropdown-content a:hover {
		background-color: #ddd;
	}

	.dropdown:hover .dropdown-content {
		display: block;
	}
</style>
