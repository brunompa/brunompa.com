<script lang="ts">
	import { formatDate } from '$lib/utils';
	export let data;
</script>

<section>
	<ul class="posts container">
		{#each data.posts as post}
			<a href={post.slug} class=" my-2">
				<li class="post grid sm:flex bg-zinc-800 rounded-l-lg rounded-r-md">
					<img
						class="mx-auto flex h-full rounded-lg p-3 sm:m-0 w-[40%]"
						alt="thumbail"
						src={post.thumbnail}
						style="aspect-ratio: 1 / 1;"
					/>
					<div class="m-3">
						<a href={post.slug} class="title text-base">{post.title}</a>
						<p class="date">{formatDate(post.date)}</p>
						<hr class="w-full h-px my-1 bg-gray-200 border-0 dark:bg-gray-700" />
						<p class="description pr-3 mt-2">{post.description}</p>
					</div>
				</li>
			</a>
		{/each}
	</ul>
</section>

<style>
	.title:hover {
		text-decoration: underline;
	}
	.posts {
		/* display: grid; */
		gap: var(--size-7);
		max-width: 720px;
	}

	.post {
		max-inline-size: var(--size-content-3);
	}

	.post:not(:last-child) {
		border-bottom: 1px solid var(--border);
		padding-bottom: var(--size-7);
	}

	.title {
		text-transform: capitalize;
	}

	.date {
		color: var(--text-2);
		font-size: 14px;
	}

	.description {
		font-size: 16px;

		overflow: hidden;
		display: -webkit-box;
		-webkit-line-clamp: 2; /* number of lines to show */
		line-clamp: 2;
		-webkit-box-orient: vertical;
	}
</style>
