<script>
	import { DarkMode } from 'flowbite-svelte';
	import '../app.postcss';
	import Navbar from '../components/navbar/Navbar.svelte';
	import { meta } from '../store/meta';

    $: innerWidth = 0
    $: meta.set({ screen: innerWidth < 850 ? 'mobile' : 'desktop' })

</script>
<svelte:window bind:innerWidth />

<div class="bg"></div>
<div class="mx-auto">
	<Navbar/>
	<div class="container mx-auto mt-20">
		<div class="m-2 bg-zinc-100 text-zinc-800 dark:text-zinc-100 dark:bg-zinc-900 rounded-md min-h-[90vh] shadow-2xl">
			<DarkMode />
			<slot />
		</div>
	</div>
</div>
