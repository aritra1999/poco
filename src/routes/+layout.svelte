<script>
	import '../app.postcss';
	import Navbar from '../components/navbar/Navbar.svelte';
</script>

<div class="bg"></div>
<div class="container mx-auto">
	<Navbar/>
	<div class="bg-zinc-100 text-zinc-800 dark:text-zinc-100 dark:bg-zinc-900 rounded-md min-h-[90vh] shadow-2xl m-2">
		<slot />
	</div>
</div>
