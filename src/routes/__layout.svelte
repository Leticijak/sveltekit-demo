<script>
	import Title from '$lib/title.svelte';
	import '../styles/global.css';
</script>

<header>
	<Title title="Kiki's gaming guides" />
</header>

<main>
	<!-- page content -->
	<slot />
</main>

<footer>
	<p>Copyright &copy; 2022 Kiki's Gaming Guides</p>
</footer>

<style>
	header {
		display: flex;
		justify-content: center;
	}
	main {
		max-width: 960px;
		margin: 20px auto;
	}
	footer {
		text-align: center;
	}
</style>
