<script lang="ts">
  import Calculadora from "./components/Calculadora.svelte";
</script>

<main>
	<Calculadora />
</main>

<style>
	:global(body) {
		background: var(--bg-900);
		overflow: hidden;
		font-family: Inter, sans-serif;
	}
		
	:root {
		--bg-900: #0D0F14;
		--bg-700: #181C25;
	}

	main {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}
</style>