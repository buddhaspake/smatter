<script lang="ts">
    export let showTitle:boolean = true;
</script>

<div class="wrapper">
    <img src="assets/applogo.png" alt="applogo" />
    {#if showTitle}
        <div class="title">Soft Matter & Microswimmers</div>
    {/if}
</div>

<style>
    div.wrapper {
        display: flex;
    }
    img { height: 2.2rem; }
    div.title {
        margin-left: 0.6rem;
        width: 10rem;
        line-height: 1.1rem;
        font-size: 1.2rem;
        font-weight: 600;
        color: #183b8d;
    }
</style>



