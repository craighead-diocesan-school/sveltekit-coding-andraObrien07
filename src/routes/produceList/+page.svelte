<script>
    import Nav from "$lib/Nav.svelte";

    import Item from "$lib/Item.svelte";
    let products = [
        {
            src: "apple.jpg",
            alt: "picture of apple",
            name: "Apple",
            price: 1.0,
            description: "red and circular",
        },
        {
            src: "banana.jpg",
            alt: "picture of banana",
            name: "Banana",
            price: 0.5,
            description: "yellow and long",
        },
        {
            src: "cherry.jpg",
            alt: "picture of cherry",
            name: "Cherry",
            price: 2.0,
            description: "dark red and circular and chokable",
        },
    ];
</script>

<Nav />

<ul>
    {#each products as product}
        <Item
            src="{product.src},"
            alt="{product.alt},"
            name="{product.name},"
            price="{product.price},"
            description="{product.description}.  "
        />
    {/each}
</ul>
