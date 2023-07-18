<script>
	import Footer from './Footer.svelte';
	import './styles.css';
</script>

<div class="app">
	<main>
		<slot />
	</main>

	<Footer />
</div>

<style>
	.app {
		padding:5px;
		background-color: var(--color-background);		
		display: flex;
		flex-direction: column;
		max-height: 100vh;
		min-height: 99vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		height: 100%;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
