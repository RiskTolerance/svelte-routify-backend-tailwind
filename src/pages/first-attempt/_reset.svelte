<script>
	import NavBar from './_components/NavBar.svelte';
</script>

<div class="nav-wrapper">
	<div class="nav">
		<NavBar />
		<!-- we load RenderStatus popup dynamically as it's not
        important and we don't want to slow down the initial load -->
		{#await import('./_components/RenderStatus.svelte') then Module}
			<svelte:component this={Module.default} />
		{/await}
	</div>
	<div class="main">
		<slot>
			<!-- optional fallback -->
		</slot>
	</div>
</div>
