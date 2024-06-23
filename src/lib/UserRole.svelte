<script>
    let role = "admin";
</script>

<main>
    <!-- This block checks if the name variable is equal to the string 'admin'. -->
    {#if role == "admin"}
        <!-- If name is equal to 'admin', this line shows an h1 element with a personalised welcome message for admin. -->
        <h1>Welcome Admin!</h1>
        <p>You have full access to the system</p>

        <!-- this block check if the role variable is equal to the string 'guest' -->
    {:else if role == "guest"}
        <!-- if role is equal to 'guest' , this line shows an h1 element with a perosnalised welcome message for guest -->
        <h1>Wecome guest</h1>
        <p>You have view-only access.</p>

        <!-- this block check if the role variable is equal to the string 'editor' -->
    {:else if role == "editor"}
        <!-- if role is equal to 'editor' , this line shows an h1 element with a perosnalised welcome message for editor -->
        <h1>Welcome, Editor!</h1>
        <p>You can edit content but have limited access.</p>

        <!-- This block specifies the content to show if the if condition is not met. -->
    {:else}
        <!-- If name is not equal to 'admin', this line shows an h1 element with a generic greeting that includes the value of the role variable. -->
        <h1>Hello, {role}!</h1>
        <p>Your access is limited</p>
    {/if}

    <label for="role">
        <input bind:value={role} placeholder="Enter role" />
        <!-- An input bound to the usd variable. The bind:value ensures that the usd variable is updated with the input value. -->
    </label>
</main>
