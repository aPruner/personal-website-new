<script>
  import Navbar from "$lib/navbar.svelte";
  import Footer from "$lib/footer.svelte";
</script>

<Navbar selectedPage="Home"/>

<div>
  <section class="bg-center bg-no-repeat bg-[url('https://flowbite.s3.amazonaws.com/docs/jumbotron/conference.jpg')] bg-gray-700 bg-blend-multiply">
    <div class="px-4 mx-auto max-w-screen-xl text-center py-24 lg:py-56">
      <h1 class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-teal-300 md:text-5xl lg:text-6xl">Adam Pruner</h1>
      <p class="mb-4 text-lg font-normal text-gray-300 lg:text-xl sm:px-16 lg:px-48">
        I'm a software generalist who specializes in full stack web applications and likes to build games for fun. I'm currently contributing my expertise to the cyber insurance industry at 
        <a href="https://coalitioninc.com" class="text-blue-600">Coalition</a>.
      </p>
    </div>
  </section>
</div>

<Footer />

<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.100);
  }
</style>

<slot />
