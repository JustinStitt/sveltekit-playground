<script>
	import { add_two } from '$lib/index';
	import Button from '$lib/components/Button.svelte';
	import { onMount } from 'svelte';
	let count = 4;

	let random_number = undefined;

	async function get_random_number() {
		const response = await fetch('/about/random-number?min=4&max=10');
		console.log(response);
		random_number = await response.json();
	}
</script>

<h1>About</h1>

<h2>{count}</h2>

<button
	on:click={() => {
		count = add_two(count, 3);
	}}>Increase Count</button
>

<button on:click={get_random_number}>Get Rando Numbo</button>
<h3>{random_number ?? 0}</h3>

<Button button_text="some text"></Button>
<Button button_text="som text"></Button>
<Button button_text="so text"></Button>

<style>
</style>
