<script context="module">
	/**
	 * @type {import('@sveltejs/kit').Load}
	 */
	export async function load({ page, fetch, session, context }) {
		const url = `http://localhost:1337/rests?rest_id=${page.params.rest}`;
		const res = await fetch(url);

		console.log('page.params.rest', page.params.rest);
		if (res.ok) {
			return {
				props: {
					rests: await res.json()
				}
			};
		}

		return {
			status: res.status,
			error: new Error(`Could not load ${url}`)
		};
	}
</script>

<script>
	export let rests;

	// console.log('rests', rests);
</script>

{#each rests as rest}
	<h1>{rest.name}</h1>

	<a sveltekit:prefetch href="/{rest.rest_id}/menu">Menu</a>
	<a sveltekit:prefetch href="/{rest.rest_id}/menu-delivery">Menu Delivery</a>
{/each}

<style>
	h1 {
		color: grey;
	}
</style>
