<script>
	import '../app.scss';
	import { page } from '$app/stores';
	import ThemeSwitch from '../lib/components/ThemeSwitch.svelte';
</script>

<header>
	<nav>
		<ul>
			<li><a href="/" class:contrast={$page.url.pathname == '/'}>Home</a></li>
		</ul>
		<ul>
			<li><ThemeSwitch /></li>
			<li><a href="/about/" class:contrast={$page.url.pathname == '/about/'}>About</a></li>
			<li><a href="/contact/" class:contrast={$page.url.pathname == '/contact/'}>Contact</a></li>
		</ul>
	</nav>
</header>

<main>
	<slot />
</main>

<footer>&copy; 2023 kpawlx</footer>
