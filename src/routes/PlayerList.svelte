<script>
	import './style.css';

	// data comes from the load function in +page.js
	export let dataset;
</script>

<ul>
	{#each dataset as player}
		<li>{player.name} ({player.team})</li>
	{/each}
</ul>	

<style>
	ul {
		width: 18em;
		max-height: 100%; /*make list no taller than parent*/
		overflow: auto; /*should enable scrolling*/
		list-style: none;
		padding: 0;
	}
	li + li {
		margin-top: 0.5em;
	}
</style>
