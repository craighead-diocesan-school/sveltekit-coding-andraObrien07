<script>
  import Nav from "$lib/Nav.svelte";
  import If from "$lib/If.svelte";
  // import UserRole from "$lib/UserRole.svelte";
  // import ProduceList from "$lib/ProduceList.svelte";
  let name = "world";
  let imageUrl = "https://picsum.photos/200";
  import ImageCard from "$lib/ImageCard.svelte";
  let isChecked = false;
  let selectedOption = "Option 1";
  let count = 0;
  import HiButton from "$lib/HiButton.svelte";
  // import NewMoney from "$lib/NewMoney.svelte";
  import EachLoops from "$lib/EachLoops.svelte";

  function up() {
    count = count + 1;
  }

  function down() {
    count = count - 1;
  }
</script>

<Nav />
<main>
  <ImageCard />

  <h1>Hello {name}!</h1>
  <img src={imageUrl} alt="Example image" />

  <input bind:value={name} placeholder="Enter your name" />
  <!-- when a name is enetered it becomes the name variable. -->

  <h1>Hello {name}!</h1>

  <input type="checkbox" bind:checked={isChecked} />
  <!-- the check box is checked -->

  <p>The checkbox is {isChecked}.</p>
  <!-- Displays the state of the checkbox. -->

  <select bind:value={selectedOption}>
    <!-- a drop down menu that is bound to selectOption in the script -->
    <option value="Option 1">Option 1</option>
    <option value="Option 2">Option 2</option>
    <option value="Option 3">Option 3</option>
  </select>

  <p>You selected: {selectedOption}</p>
  <!--  Displays the selected option. -->

  <!-- Displays the current count. -->
  <p>Count: {count}</p>
  <!-- Buttons that call the up and down functions when clicked, updating the count. -->
  <button on:click={up}>up</button>
  <button on:click={down}>down</button>

  <HiButton />

  <If />

  <EachLoops />
  <!-- <ProduceList /> -->
</main>

<style>
  main {
    background-image: url("Screenshot.JPG");
    background-position: cover;
  }
  p {
    color: aliceblue;
  }
</style>
