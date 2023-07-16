<script>
	import Navbar from '$lib/navbar.svelte';
	import Footer from '$lib/footer.svelte';
	import '../app.css';
	import { page } from '$app/stores';
</script>

<Navbar currentPagePath={$page.url.pathname} />

<div>
	<section class="relative flex items-center justify-center min-h-screen overflow-hidden">
		<div class="z-30 relative px-4 mx-auto max-w-screen-xl text-center py-24 lg:py-56">
			<slot />
		</div>

		<video autoplay loop muted class="z-10 absolute w-auto min-w-full min-h-full max-w-none">
			<source src="https://imgur.com/ubXmpt8.mp4" type="video/mp4" />
		</video>
	</section>
</div>

<Footer />
