<script lang="ts">
	import * as config from '$lib/config';
	import '../app.css';
	import Toggle from './toggle.svelte';
</script>

<div class="top-links">
	<a target="_blank" href="https://larryfisherman.click">larryfisherman</a>
	<a target="_blank" href="https://strategykeyboard.brunompa.com">strategykeyboard_</a>
	<a target="_blank" href="https://twitter.com/bruno_mpa">twitter</a>
</div>

<nav
	class="bg-gradient-to-br from-black to-transparent dark:from-[#383A3C] dark:to-transparent w-full z-20 top-5 left-0"
>
	<div class=" flex items-center justify-between mx-auto py-1 px-4">
		<a href="/" class="flex items-center">
			<span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white"
				>{config.title}</span
			>
		</a>

		<div class=" w-min items-center justify-between md:flex md:w-auto md:order-0">
			<ul class="flex p-4 md:p-0 font-medium rounded-lg md:flex-row md:space-x-8 md:mt-0">
				<li>
					<a
						href="/blog"
						class="block py-2 pl-3 pr-4 text-gray-900 rounded md:p-0 dark:text-white dark:border-gray-700"
						>blog</a
					>
				</li>
				<li>
					<a
						href="rss.xml"
						class="block py-2 pl-3 pr-4 text-gray-900 rounded md:p-0 dark:text-white dark:border-gray-700"
						target="_blank">RSS</a
					>
				</li>
			</ul>
		</div>
		<!-- <Toggle /> -->
	</div>
</nav>
