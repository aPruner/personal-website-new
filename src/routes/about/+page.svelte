<script>
  import Navbar from "$lib/navbar.svelte";
</script>

<Navbar selectedPage="About"/>
<h1 class="text-3xl font-bold">Adam Pruner</h1>
<p>Software Engineer + Game Developer</p>

<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.100);
  }
</style>

<slot />
