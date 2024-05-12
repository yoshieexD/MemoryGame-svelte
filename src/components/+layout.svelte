<script lang="js">
    import Navbar from "./navbar/+navbar.svelte";
    export let title;
</script>

<svelte:head>
    <title>{title}</title>
</svelte:head>
<div>
    <Navbar />
    <slot />
</div>
