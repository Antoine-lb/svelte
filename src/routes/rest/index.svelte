<script context="module">
	/**
	 * @type {import('@sveltejs/kit').Load}
	 */
	// export async function load({ page, fetch, session, context }) {
	// 	const url = `https://bc-backend-prod.herokuapp.com/rests?rest_id=${page.params.rest}`;
	// 	const res = await fetch(url);

	// 	console.log('page.params.rest', page.params.rest);
	// 	if (res.ok) {
	// 		return {
	// 			props: {
	// 				rests: await res.json()
	// 			}
	// 		};
	// 	}

	// 	return {
	// 		status: res.status,
	// 		error: new Error(`Could not load ${url}`)
	// 	};
	// }
</script>

<h1>Rest Main Page</h1>

<a sveltekit:prefetch href="/rest/menu">Menu</a>
<a sveltekit:prefetch href="/rest/menu-delivery">Menu Delivery</a>

<style>
	h1 {
		color: grey;
	}
</style>
