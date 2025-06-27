<script>
	import '../app.css';
    import Navbar from './navbar.svelte';
	let { children } = $props();
</script>
<Navbar/>
{@render children()}
