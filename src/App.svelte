<script>
	import Tailwindcss from './Tailwindcss.svelte';
	import Nav from './components/Nav.svelte';
	import Button from './components/Button.svelte';
	import Card from './components/Card.svelte';
</script>

<svelte:head>
	<style>
		body {
			@apply bg-gradient-to-r from-green-600 via-green-400 to-green-600;
		}
	</style>
</svelte:head>

<Tailwindcss />
<div class="flex justify-center my-10">
	<Nav />
</div>
<div class="flex flex-col justify-around space-y-10">
	<div class="dealer flex justify-center space-x-4">
		<Card value={"h2"} showBack={true}/>
		<Card value={"d5"}/>
	</div>

	<div class="game-controls flex flex-col justify-around items-center">
		
		<!-- Dealer total -->
		<span class="font-bold">Dealer</span>
		<div class="totals">
			<span>10</span>
		</div>

		<div class="controls my-6 space-x-4">
			<Button><i class="fas fa-plus-square"></i> Hit</Button>
			<Button><i class="fas fa-money-bill-wave"></i> Double</Button>
			<Button><i class="fas fa-hand-paper"></i> Stand</Button>
		</div>

		<!-- Player total -->
		<div class="totals">
			<span>10</span>
		</div>
		<span class="font-bold">Player</span>
	</div>

	<div class="player flex justify-center space-x-4">
		<Card value={"c10"}/>
		<Card value={"h7"}/>
	</div>
</div>

<style lang="postcss">
	.totals {
		@apply p-4 leading-none text-center shadow-inner rounded mt-1 font-bold text-xl flex flex-col justify-center items-center bg-green-500 ;
	}
</style>
