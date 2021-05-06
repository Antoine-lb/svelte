<script>
	import { slide } from 'svelte/transition';
	export let title;
	export let id;

	let isOpen = true;

	function toggleOpen() {
		isOpen = !isOpen;
	}
</script>

<button on:click={toggleOpen}>
	<svg
		class:point-down={isOpen === true}
		class:point-up={isOpen === false}
		xmlns="http://www.w3.org/2000/svg"
		width="18"
		height="18"
		viewBox="0 0 24 24"
		><path d="M0 7.33l2.829-2.83 9.175 9.339 9.167-9.339 2.829 2.83-11.996 12.17z" /></svg
	>
	<h2 {id}>{title}</h2>
</button>
{#if isOpen}
	<div transition:slide><slot /></div>
{/if}

<style>
	button {
		background: none;
		border: none;
		display: flex;
		align-items: center;
	}

	h2 {
		font-size: 25px;
		color: rgb(62, 62, 62);
		margin-left: 10px;
	}

	path {
		fill: rgb(62, 62, 62);
	}

	.point-up {
		transform: rotate(180deg);
		transition-duration: 0.3s;
	}
	.point-down {
		transform: rotate(0deg);
		transition-duration: 0.3s;
	}
</style>
