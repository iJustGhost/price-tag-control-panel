<script>
    let name = $state();
    let price = $state();
    let ip = $state();

    async function updateTag() {
        await fetch(`http://${ip}/update?name=${name}&price=${price}`);
    }

</script>

<input type="text" name="name" id="" bind:value={name}>
<input type="text" name="price" id="" bind:value={price}>
<input type="text" name="ip" id="" bind:value={ip}>
<button onclick={updateTag}>Submit</button>