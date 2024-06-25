<script>
    export let name;
    export let price;
    export let description;
    export let src;
    export let alt;
</script>

<!-- <img {src} {alt} />
{name} ${price}
{description} -->

<div class="column">
    <img {src} {alt} />
    <div class="words">
        <p class="name">
            {name}
        </p>
        <p class="price">${price} {description}</p>
    </div>
</div>

<style>
    .words {
        margin-left: 60px;
        margin-top: 100px;
    }
    img {
        width: 500px;
        margin-top: 20px;
        margin-bottom: 20px;
        display: flex;
    }
    .column {
        display: flex;
    }
    p {
        font-family: "Passero One";
        font-size: 40px;
        margin-bottom: 10px;
        width: fit-content;
    }

    .price {
        font-size: 35px;
    }
</style>
