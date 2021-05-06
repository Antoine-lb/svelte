<script>
	export let id = '1';
	export let title = 'title';
	export let description = 'description';
	export let price = '1.00';
	export let img = '1.00';
</script>

<div class="main-container" {id}>
	<div>
		<h4>{title}</h4>
		<p class="description">{description}</p>
		<p class="price">${price}</p>
		<div class="divider" />
	</div>
	<div class="img-container">
		<img width="65" height="65" alt={title} src={img} />
	</div>
</div>

<style>
	.main-container {
		display: flex;
		padding: 10px;
	}
	h4 {
		margin: 0;
	}
	p {
		margin: 5px;
	}
	.description {
		overflow: hidden;
		line-height: 20px;
		height: 40px;
		text-overflow: ellipsis;
		display: -webkit-box;
		-webkit-line-clamp: 2;
		-webkit-box-orient: vertical;
	}

	.price {
		font-style: italic;
	}

	.img-container {
		/* margin-right: 10px; */
		margin-top: 5px;
	}
	img {
		border-radius: 3px;
		box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.19);
	}
	.divider {
		margin: auto;
		margin-top: 15px;
		border-bottom: 1.5px solid rgb(210, 210, 210);
		width: 70%;
	}
</style>
