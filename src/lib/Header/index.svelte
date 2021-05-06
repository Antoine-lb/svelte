<script lang="ts">
	import { page } from '$app/stores';
</script>

<header>
	<nav>
		<a sveltekit:prefetch href="/">Home</a>
	</nav>
</header>

<style>
	header {
		display: flex;
		align-items: center;
		justify-content: center;
		background-color: #732619;
		height: 30px;
	}

	a {
		color: white;
		text-decoration: none;
	}
</style>
