<script lang="ts">
    import { activePage } from "../assets/stores";

    export let name = "NavBarElement";
    export let link = "/";
    export let codename = "home";

    const changeActivePage = (codename: string) => {
        activePage.set(codename);
    };
</script>

<li class="nav-item">
    <a
        class="nav-link active"
        aria-current="page"
        href={link}
        on:click={() => changeActivePage(codename)}>{name}</a
    >
</li>
