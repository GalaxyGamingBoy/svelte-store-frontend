<script lang="ts">
    import { onMount } from "svelte";
    import axios from "axios";
    import Card from "./Card.svelte";

    let products = [];

    onMount(async () => {
        const { data } = await axios.get("http://localhost:5050/getProducts");
        products = data;
    });
</script>

<div class="d-flex justify-content-center">
    <h1 class="p-4">Home</h1>
    <br />
</div>

<div class="d-flex justify-content-center">
    <div>
        <div class="row">
            {#each products as product}
                <Card
                    title={product.name}
                    price={product.price}
                    stock={product.stock}
                />
                <br />
            {/each}
        </div>
    </div>
</div>
