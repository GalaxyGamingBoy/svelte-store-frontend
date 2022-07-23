<script lang="ts">
    import NavBarElement from "./NavBarElement.svelte";
    export let layout = {};
</script>

<nav class="navbar navbar-expand-lg bg-light">
    <div class="container-fluid">
        <a class="navbar-brand" href="/">GStore</a>
        <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent"
            aria-expanded="false"
            aria-label="Toggle navigation"
        >
            <span class="navbar-toggler-icon" />
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                {#each layout.navbar as navbarElement}
                    <NavBarElement
                        name={navbarElement.name}
                        link={navbarElement.link}
                        codename={navbarElement.codename}
                    />
                {/each}
            </ul>
        </div>
    </div>
    <!-- <span class="navbar-text">
        <NavBarElement
            name={layout.navbar[2].name}
            link={layout.navbar[2].link}
            codename={layout.navbar.codename}
        />
    </span> -->
    {#each layout.navbarRight as navbarElement}
        <span class="navbar-text" style="padding: 15px;">
            <NavBarElement
                name={navbarElement.name}
                link={navbarElement.link}
                codename={navbarElement.codename}
            />
        </span>
    {/each}
</nav>
