<script>
    let workers = ["Andra", "Emma", "G", "Ray", "Ms Mulverhill"];
</script>

<ul>
    {#each workers as worker, index}
        <!-- This block iterates over the workers array and assigns each item to the work variable. -->

        <!-- the index variable provides the position of each item in the array, starting from 0. -->
        <li>{index + 1}. {worker}</li>
        <!-- For each item in the array, this line renders a list item (li) containing the workers name. -->
    {/each}
</ul>
