<script>
    let usd = "";
    let nzld = "";
    nzld = Number(nzld);

    usd = Number(usd);
    function changer() {
        nzld = 1.63 * usd;
    }
</script>

<main>
    <label for="usd">
        <input bind:value={usd} placeholder="Enter usd" />
    </label>

    <p>{nzld}</p>
    <button on:click={changer}>Convert</button>
</main>

<style>
    button {
        width: 10rem;
        height: 10rem;
        margin: 3rem 3rem;
        border: none;
        border-radius: 50px;
        background: linear-gradient(145deg, #cacaca, #f0f0f0);
        box-shadow:
            10px 10px 30px #bebebe,
            -10px -10px 30px #ffffff;
    }

    button:active {
        box-shadow:
            inset 20px 20px 60px #bebebe,
            inset -20px -20px 60px #ffffff;
    }

    :global(*) {
        background: #e0e0e0;
    }
</style>
