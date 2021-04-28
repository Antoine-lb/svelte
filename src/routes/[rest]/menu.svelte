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
	let rest = rests[0];

	let product_categories = rest.product_categories;

	// console.log('rests', rests);
</script>

<h1>{rest.name} Menu Delivery</h1>
<ul>
	{#each product_categories as categories}
		<li>{categories.title}</li>
	{/each}
</ul>

<style>
	h1 {
		color: grey;
	}
</style>
