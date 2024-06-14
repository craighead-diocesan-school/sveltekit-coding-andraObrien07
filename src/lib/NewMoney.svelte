<script>
    let usd = "";
    //storing the input that the user inputs for usd
    usd = Number(usd);

    let nzld = "";
    //storing the converted usd to nzld
    nzld = Number(nzld);

    const ConvR = 1.63;
    // usd to nzld conversion rate as a constant because it doesnt change

    // function connected to the button
    function changer() {
        nzld = ConvR * usd;
        // This function multiplies the usd value by the conversion rate ConvR and assigns the result to nzld.
    }
</script>

<main>
    <label for="usd">
        <input bind:value={usd} placeholder="Enter usd" />
        <!-- An input bound to the usd variable. The bind:value ensures that the usd variable is updated with the input value. -->
    </label>

    <!-- Displays the value of nzld, which is the result of the conversion from USD to NZD. -->
    <p>{nzld}</p>
    <button on:click={changer}>Convert</button>
    <!-- A button that calls the changer function when clicked. This triggers the conversion of USD to NZD. -->
</main>

<style>
    /* button style */
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

    /* :global(*) {
        background: #e0e0e0;
    } */
</style>
