<script>
	import Clock from './Clock.svelte';
</script>

<section class="app">
	<Clock />
</section>

<style>
	:global(body),
	* {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	.app {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
		width: 100vw;
	}
</style>
