<script lang="ts">
    import layout from "./assets/layout.json";
    import NavBar from "./lib/NavBar.svelte";
    import Home from "./lib/Home.svelte";
    import About from "./lib/About.svelte";

    import { activePage } from "./assets/stores";
</script>

<main>
    <NavBar {layout} />
    {#if $activePage === "home"}
        <Home />
    {:else if $activePage === "about"}
        <About />
    {/if}
</main>

<style>
</style>
