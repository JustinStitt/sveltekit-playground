<script>
	export let button_text; // prop
	// prop means you can pass it in when creating the component elsewhere
</script>

<button id="my-button">
	{button_text}
</button>

<style>
	#my-button {
		background-color: green;
		border-radius: 15px;
		border-color: red;
	}
</style>
