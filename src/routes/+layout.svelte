<script lang="ts">
	import AppHeader from "$lib/AppHeader.svelte";
    let { children } = $props();
    let showTitle: boolean = false;
</script>

<div class="wrapper">
    <nav>
        <AppHeader showTitle={showTitle} />
        <div class="spacer"></div>
        <a href="/">Home</a>
        <a href="/research">Research</a>
        <a href="/publications">Publications</a>
        <a href="/team">Team</a>
        <a href="/join">Join!</a>
        <a href="/teaching">Teaching</a>
        <a href="/gallery">Gallery</a>
    </nav>
    <main>
        {@render children()}
    </main>
</div>

<style>
    :global(body) {
        /* Site-specific */
        font-family: 'Segoe UI', Tahoma, sans-serif; 
        color: #2c2c2c;
    }
    nav {
        padding: 1rem;
        display: flex;
    }
    nav a {
        margin-left: 0.8rem;
        text-transform: uppercase;
        color: currentColor;
        text-decoration: none;
    }
    nav a:hover {
        color: #3a80e3;
    }
    .spacer { flex-grow: 1 }
    
    main {
        padding: 2rem 1rem; 
    }
</style>
