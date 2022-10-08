<script lang="ts">
	import '../app.css'
	type Product = {
		name: string
		quantity: number
	}
	let products: Product[] = [
		{ name: 't-shirt', quantity: 10 },
		{ name: 'mug', quantity: 30 },
		{ name: 'sticker', quantity: 8 },
		{ name: 'sweatshirt', quantity: 12 }
	]
	function addProduct() {
		let cup: Product = { name: 'cup', quantity: 4 }
		products = [cup, ...products]
	}
</script>

<button on:click={addProduct}>Add product</button>
{#each products as product, index (product.name)}
	<h3>{product.name}</h3>
	<input type="checkbox" />
	<p>{index}</p>
{/each}
