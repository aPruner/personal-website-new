<script>
	import Navbar from '$lib/navbar.svelte';
	import Footer from '$lib/footer.svelte';
</script>

<Navbar selectedPage="Home" />

<div>
	<section class="relative flex items-center justify-center min-h-screen overflow-hidden">
		<div class="z-30 relative px-4 mx-auto max-w-screen-xl text-center py-24 lg:py-56">
			<h1
				class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-teal-200 md:text-5xl lg:text-6xl"
			>
				Adam Pruner
			</h1>
			<p class="mb-4 text-lg font-normal text-gray-300 lg:text-xl sm:px-16 lg:px-48">
				I'm a software generalist who specializes in full stack web applications and likes to build
				games for fun. I'm currently contributing my expertise to the growth engineering team at
				<a href="https://coalitioninc.com" class="text-blue-500">Coalition</a>.
			</p>
			<a
				href="/contact"
				class="inline-flex justify-center items-center py-3 px-5 mr-2 text-base font-medium text-center text-white rounded-lg bg-teal-600 hover:bg-cyan-800 focus:ring-4 focus:ring-blue-300 dark:focus:ring-blue-900"
			>
				Let's chat
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="currentColor"
					class="ml-1.5 mt-1 mb-0.5 w-6 h-6"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75"
					/>
				</svg>
			</a>
			<a
				href="https://linkedin.com/in/adam-pruner"
				class="inline-flex justify-center items-center py-3 px-5 mr-2 text-base font-medium text-center text-white rounded-lg bg-teal-600 hover:bg-cyan-800 focus:ring-4 focus:ring-blue-300 dark:focus:ring-blue-900"
			>
				Let's connect
				<svg
					xmlns="http://www.w3.org/2000/svg"
					viewBox="0 0 30 30"
					width="30px"
					height="30px"
					fill="#FFFFFF"
					class="ml-1"
				>
					<path
						d="M24,4H6C4.895,4,4,4.895,4,6v18c0,1.105,0.895,2,2,2h18c1.105,0,2-0.895,2-2V6C26,4.895,25.105,4,24,4z M10.954,22h-2.95 v-9.492h2.95V22z M9.449,11.151c-0.951,0-1.72-0.771-1.72-1.72c0-0.949,0.77-1.719,1.72-1.719c0.948,0,1.719,0.771,1.719,1.719 C11.168,10.38,10.397,11.151,9.449,11.151z M22.004,22h-2.948v-4.616c0-1.101-0.02-2.517-1.533-2.517 c-1.535,0-1.771,1.199-1.771,2.437V22h-2.948v-9.492h2.83v1.297h0.04c0.394-0.746,1.356-1.533,2.791-1.533 c2.987,0,3.539,1.966,3.539,4.522V22z"
					/></svg
				>
			</a>
		</div>
	
		<video autoplay loop muted class="z-10 absolute w-auto min-w-full min-h-full max-w-none">
			<source src="https://imgur.com/rYft513.mp4" type="video/mp4" />
		</video>
</section>
</div>

<Footer />

<slot />

<style lang="postcss">
	:global(html) {
		background-color: theme(colors.gray.100);
	}
</style>
