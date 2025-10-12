<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/Besicon.png';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<title>Bes-Ar Putri</title>
</svelte:head>

{@render children?.()}
