<script lang="ts">
	import { formatDate } from '$lib/utils';

	export let data;
</script>

<svelte:head>
	<title>{data.meta.title}</title>
	<meta property="og:type" content="article" />
	<meta property="og:title" content={data.meta.title} />
	<meta property="og:type" content="article" />
	<meta
		property="og:image"
		content={'https://brunompa.com/blog/' +
			data.meta.thumbnail.substring(data.meta.thumbnail.indexOf('blog') + 5)}
	/>
</svelte:head>

<article class="px-4 lg:px-0 mx-auto">
	<hgroup>
		<h1>{data.meta.title}</h1>
		<p class="text-sm">Published at {formatDate(data.meta.date)}</p>
	</hgroup>

	<div class="prose prose-invert mt-4">
		<svelte:component this={data.content} />
	</div>
</article>

<style>
	article {
		max-inline-size: var(--size-content-3);
		margin-inline: auto;
	}

	hgroup {
		max-width: 52ch;
	}

	article {
		max-width: 65ch;
	}

	h1 {
		text-transform: capitalize;
	}

	h1 + p {
		margin-top: var(--size-2);
		color: var(--text-2);
	}
</style>
