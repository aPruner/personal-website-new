<script>
</script>

<h1
	class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-teal-200 md:text-5xl lg:text-6xl"
>
	Send me an email
</h1>

<div class="text-left">
	<label for="email" class="block text-lg font-large leading-6 text-white">Email</label>
	<div class="relative mt-2 rounded-md shadow-sm">
		<input
			type="text"
			name="email"
			id="email"
			class="block w-full rounded-md border-0 py-1.5 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
			placeholder="johndoe@gmail.com"
		/>
	</div>

	<label for="message" class="block mt-2 text-lg font-large leading-6 text-white">Message</label>
	<div class="relative mt-2 rounded-md shadow-sm">
		<textarea
			name="message"
			id="message"
			class="block w-full rounded-md border-0 py-2.5 h-24 resize-none text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-4"
			placeholder="Write your message here..."
		/>
	</div>

	<button class="bg-teal-500 hover:bg-cyan-800 mt-4 text-white py-2 px-4 rounded">
		Send it!
	</button>
</div>

<style lang="postcss">
	:global(html) {
		background-color: theme(colors.gray.100);
	}
</style>
