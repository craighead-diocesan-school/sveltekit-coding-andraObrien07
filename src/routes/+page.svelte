<script>
  let name = "world";
  let imageUrl = "https://picsum.photos/200";
  import ImageCard from "$lib/ImageCard.svelte";
  let isChecked = false;
  let selectedOption = "Option 1";
  let count = 0;
  import HiButton from "$lib/HiButton.svelte";
  import NewMoney from "$lib/NewMoney.svelte";
  function up() {
    count = count + 1;
  }

  function down() {
    count = count - 1;
  }
</script>

<main>
  <ImageCard />

  <h1>Hello {name}!</h1>
  <img src={imageUrl} alt="Example image" />

  <input bind:value={name} placeholder="Enter your name" />

  <h1>Hello {name}!</h1>

  <input type="checkbox" bind:checked={isChecked} />

  <p>The checkbox is {isChecked}.</p>

  <select bind:value={selectedOption}>
    <option value="Option 1">Option 1</option>
    <option value="Option 2">Option 2</option>
    <option value="Option 3">Option 3</option>
  </select>

  <p>You selected: {selectedOption}</p>

  <p>Count: {count}</p>
  <button on:click={up}>up</button>
  <button on:click={down}>down</button>

  <HiButton />
  <NewMoney />
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
