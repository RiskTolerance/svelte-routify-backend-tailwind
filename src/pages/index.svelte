<script>
	import RoutifyIntro from './example/_components/RoutifyIntro.svelte';
	import NewApp from './first-attempt/_components/Entry.svelte';
	import { metatags } from '@roxi/routify';
	metatags.title = 'My Routify app';
	metatags.description = 'Description coming soon...';
</script>

<RoutifyIntro />
<NewApp />
