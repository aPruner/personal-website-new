<script>
	import avatarImg from './images/me.png';
	import resume from './assets/resume.pdf';

	let pages = new Map(
		Object.entries({
			'/': 'Home',
			'/about': 'About',
			'/projects': 'Projects',
			'/resume': 'Resume',
			'/contact': 'Contact'
		})
	);

	/** @type {string} */
	export let currentPagePath;
	const commonPageStyles = 'rounded-md px-3 py-2 text-sm font-medium';
	const mobileMenuPageStyles = 'block rounded-md px-3 py-2 text-base font-medium';
	const pageClass = `text-gray-300 hover:bg-gray-700 hover:text-white ${commonPageStyles}`;
	const currentPageClass = `bg-gray-900 text-white ${commonPageStyles}`;
	const mobileMenuPageClass = `text-gray-300 hover:bg-gray-700 hover:text-white ${mobileMenuPageStyles}`;
	const mobileMenuCurrentPageClass = `bg-gray-900 text-white ${mobileMenuPageStyles}`;

	let isMobileMenuOpen = false;

	const toggleMobileMenuOpen = () => {
		isMobileMenuOpen = !isMobileMenuOpen;
	};
</script>

<nav class="bg-slate-800">
	<div class="mx-auto px-2 sm:px-6 lg:px-8">
		<div class="relative flex h-16 items-center justify-between">
			<div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
				<!-- Mobile menu button-->
				<button
					type="button"
					on:click={toggleMobileMenuOpen}
					class="inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
					aria-controls="mobile-menu"
					aria-expanded="false"
				>
					<span class="sr-only">Open main menu</span>
					<svg
						class={`${!isMobileMenuOpen ? 'block' : 'hidden'} h-6 w-6`}
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
						/>
					</svg>
					<svg
						class={`${isMobileMenuOpen ? 'block' : 'hidden'} h-6 w-6`}
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
					</svg>
				</button>
			</div>

			<div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
				<div class="flex flex-shrink-0 items-center">
					<a href="/">
						<img
							class="inline-block h-10 w-10 rounded-full ring-1 ring-cyan-300"
							src={avatarImg}
							alt="Adam Pruner"
						/>
					</a>
				</div>
			</div>

			<div
				class="hidden sm:flex flex-1 items-center justify-center sm:items-stretch sm:justify-end"
			>
				<div class="hidden sm:ml-6 sm:block">
					<div class="flex space-x-4">
						{#each [...pages] as [path, name]}
							<a
								target={path === '/resume' ? '_blank' : null}
								href={path === '/resume' ? resume : path}
								class={pages.get(currentPagePath) === name ? currentPageClass : pageClass}
								aria-current={pages.get(currentPagePath) === name && 'page'}>{name}</a
							>
						{/each}
					</div>
				</div>
			</div>
		</div>
	</div>

	<!-- Mobile menu, show/hide based on menu state. -->
	<div class="sm:hidden" id="mobile-menu" style={!isMobileMenuOpen ? 'display: none' : null}>
		<div class="space-y-1 px-2 pb-3 pt-2">
			{#each [...pages] as [path, name]}
				<a
					href={path}
					class={pages.get(currentPagePath) === name
						? mobileMenuCurrentPageClass
						: mobileMenuPageClass}
					aria-current={pages.get(currentPagePath) === name && 'page'}>{name}</a
				>
			{/each}
		</div>
	</div>
</nav>

<style lang="postcss">
	:global(html) {
		background-color: theme(colors.gray.100);
	}
</style>
