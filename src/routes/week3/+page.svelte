<script>
	import Navbar from '$lib/molecules/navigation.svelte';

	import { writable } from 'svelte/store';

	export let data;
	export const test = writable(1);

	console.log(data);
</script>

<Navbar />

<main>
		<p>Wens</p>

</main>

<style>
	
</style>
