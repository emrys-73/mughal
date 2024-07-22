<script>
	import '../app.css';
	import Button from '$lib/components/ui/button/button.svelte';

	const menu = [
		{
			name: 'Speisekarte',
			href: '/#menu',
			highlight: false,
		},
		{
			name: 'Gallerie',
			href: '/#gallerie',
			highlight: false,
		},
		{
			name: 'Hotel',
			href: 'https://direct-book.com/properties/mughalhotel-restaurant?locale=de&items%5B0%5D%5Badults%5D=2&items%5B0%5D%5Bchildren%5D=0&items%5B0%5D%5Binfants%5D=0&currency=EUR&checkInDate=2024-07-17&checkOutDate=2024-07-18&trackPage=no&selected=0',
			highlight: false,
		},
		{
			name: 'Reservieren',
			href: '/#contact',
			highlight: true,
		},
	]

</script>


<div class="w-full h-full min-h-screen flex flex-col relative">
	<div class="w-full h-16 backdrop-blur-md px-4 flex flex-row fixed top-0 justify-between items-center z-30 bg-[#120E0B] bg-opacity-30">
		<div class="h-full flex flex-col justify-center items-center">
			<a href="/" class="opacity-80 hover:opacity-100 transition-all duration-500 ease-in-out">
				<img src="/logo.png" alt="M">
			</a>
		</div>

		<div class="w-3/5 h-full justify-around items-center flex flex-row z-40">
			{#each menu as m}
				<div class="flex z-40">
					<Button href="{m.href}" class="{m.highlight ? 'bg-[#800707] px-10 py-2 rounded-full hover:bg-[#120E0B]' : 'bg-transparent hover:bg-transparent text-opacity-80 hover:text-opacity-100'} text-white text-md font-light transition-all ease-in-out duration-500">{m.name}</Button>
				</div>
			{/each}
		</div>
	</div>

	<slot/>
</div>


