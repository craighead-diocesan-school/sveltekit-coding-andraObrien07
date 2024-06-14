<script>
    // This variable will store the welcome message.
    let welcomemessage = "";

    function sayhi() {
        // A function that sets the welcomemessage variable to "Hi!".

        welcomemessage = "Hi!";
    }
</script>

<main>
    <!-- Displays the value of welcomemessage. Initially, this will be empty, but will change to "Hi!" when the button is clicked. -->
    <p>{welcomemessage}</p>

    <!-- A button that calls the sayhi function when clicked. This updates the welcomemessage to "Hi!". -->
    <button on:click={sayhi}>Press Me</button>
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
        /* Box shadows create a 3D effect, with different shadows applied when the button is active  */
        box-shadow:
            inset 20px 20px 60px #bebebe,
            inset -20px -20px 60px #ffffff;
    }
</style>
