<script>
    //defining the name variable
    let name = "bob";
</script>

<main>
    <!-- //This block checks if the name variable has a truthy value. -->
    {#if name}
        <h1>Hello, {name}!</h1>
        <!-- If name is truthy, this line renders an h1 element with the personalised greeting. -->
    {:else}
        <!-- This block specifies the content to render if the if condition is not met. -->
        <h1>Hello, stranger!</h1>
        <!-- If name is falsy, this line renders an h1 element with the generic greeting -->
    {/if}
    <!-- This closes the if block. -->

    <!-- This block checks if the name variable is equal to the string 'Alice'. -->
    {#if name == "Alice"}
        <!-- If name is equal to 'Alice', this line shows an h1 element with a personalised welcome message for Alice. -->
        <h1>Welcome back, Alice!</h1>

        <!-- this block check if the name variable is equal to the string 'bob' -->
    {:else if name == "bob"}
        <!-- if name is equal to 'bob' , this line shows an h1 element with a perosnalised welcome message for bob -->
        <h1>Not you again!</h1>

        <!-- This block specifies the content to show if the if condition is not met. -->
    {:else}
        <!-- If name is not equal to 'Alice', this line shows an h1 element with a generic greeting that includes the value of the name variable. -->
        <h1>Hello, {name}!</h1>
    {/if}
</main>
