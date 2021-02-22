<script>
	import { url, isActive } from '@roxi/routify';
	const _links = [
		['/', 'Retunr to dir |'],
		['./index', 'Home |'],
		['./page1', 'Page1 |'],
		['./page2', 'Page2 |'],
		['./page3', 'Page3'],
	];
</script>

{#each _links as [path, name]}
	<a class="link" class:active={$isActive(path)} href={$url(path)}>
		{name}
	</a>
{/each}

<style>
    .active {
        color: red;
    }
</style>
