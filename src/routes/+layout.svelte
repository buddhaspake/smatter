<script lang="ts">
	import AppHeader from "$lib/AppHeader.svelte";
    let { children } = $props();
    let showTitle: boolean = false;
</script>

<nav>
    <AppHeader showTitle={showTitle} />
    <div class="spacer"></div>
    <a href="/">Home</a>
    <a href="/about">About</a>
</nav>

<style>
    :global(body) {
        /* Site-specific */
        font-family: 'Segoe UI', Tahoma, sans-serif; 
    }
    nav {
        padding: 0.6rem;
        display: flex;
    }
    nav a {
        margin-left: 0.8rem;
        text-transform: uppercase;
        text-decoration: none;
    }
    .spacer { flex-grow: 1 }
</style>

{@render children()}
