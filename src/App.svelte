<script>
	import Tailwindcss from './Tailwindcss.svelte';
	import Card from './components/Card.svelte';

	let cards = new Array(13)
	let prefix = "C"
</script>

<Tailwindcss />
<main class="flex bg-green-500 h-screen items-center justify-center">

	<Card value={"c1"}/>
	<Card value={"h1"} bt={1}/>
	<Card value={"s1"} bt={2}/>
	<Card value={"d1"} bt={3}/>

	<!-- {#each cards as card, i}
		<Card value={prefix + (i+1)} />
	{/each} -->
</main>

<style>
</style>
