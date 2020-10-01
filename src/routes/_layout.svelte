<script>
	import Nav from '../components/nav.svelte';

	export let segment;
</script>

<style>
	
</style>

<Nav {segment}/>

<main>
	<slot></slot>
</main>