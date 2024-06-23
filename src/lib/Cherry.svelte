<script>
    export let name;
    ("Apple");
    export let price;
    1.0;
    export let description;
    ("red and circular");
</script>

<ul>
    {#each products as product}
        <li>{product.name} ${product.price} {product.description}</li>
    {/each}
</ul>
