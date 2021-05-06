<script context="module">
	/**
	 * @type {import('@sveltejs/kit').Load}
	 */

	import MenuNav from '$lib/MenuNav/index.svelte';
	import Collapse from '$lib/Collapse/index.svelte';
	import Product from '$lib/Product/index.svelte';
</script>

<MenuNav />
<h1>Menu</h1>
<Collapse title={'Platos'} id={'platos'}>
	<Product
		id="ostras"
		title="Ostras"
		description="12 Ostras 'Corrientes' recién abiertas montadas en plato, acompañadas de un limón."
		price="10.000"
		img="https://bc-site-prod.s3.us-west-1.amazonaws.com/Ostras_1_9888448261.jpg"
	/>
	<Product
		id="Salmón al Eneldo"
		title="Salmón al Eneldo"
		description="Finas láminas de salmón marinado, terminado con aceite de eneldo."
		price="7.000"
		img="https://bc-site-prod.s3.us-west-1.amazonaws.com/Whats_App_Image_2020_08_10_at_13_09_24_2_1b80e3ef5b.jpeg"
	/>
	<Product
		id="Tostadas de Pan"
		title="Tostadas de Pan"
		description="12 Tostadas de pan de masa madre de alta hidratación."
		price="3.500"
		img="https://bc-site-prod.s3.us-west-1.amazonaws.com/tostadas_f2f1dbb66a.jpeg"
	/>
	<Product
		id="Plato 3 Quesos"
		title="Plato 3 Quesos"
		description="Plato 3 quesos: Brillat Savarin, Beaufort y Roquefort."
		price="10.000"
		img="https://bc-site-prod.s3.us-west-1.amazonaws.com/TABLA_DE_QUESO_1_7318f21319.png"
	/>
</Collapse>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2 id="entradas">Emtradas</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>
<h2>Smomete</h2>

<style>
	h1 {
		color: grey;
	}
</style>
