<script>
    let products = [
        { name: "Apple", price: 1.0, description: "red and circular" },
        { name: "Banana", price: 0.5, description: "yellow and long" },
        {
            name: "Cherry",
            price: 2.0,
            description: "dark red and circular and chokable",
        },
    ];

    import Cherry from "$lib/cherry.svelte";
</script>

<ul>
    {#each products as product}
        <li>{product.name} ${product.price} {product.description}</li>
    {/each}
</ul>
