<script>
	import Header from './components/Header.svelte';
	import Writing from './components/Writing.svelte';
	import Maps from './components/Maps.svelte'
	
	let clickedButton = '';

	function clickMaps() {
		clickedButton = 'maps';
	}
	function clickWriting()	{
		clickedButton = 'writing';
	}
</script>

<style>
	.main-buttons {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		text-align: center;
		align-items: center;
		padding-top: 5vh;
	}

	button {
		border: none;
		background: none;
		cursor: pointer;
	}
</style>
<Header/>

<div>
<div class="main-buttons">
	<button class="title" on:click={clickMaps}>Maps <br> 地図</button>
	<button class="title" on:click={clickWriting}>Writing <br> 文章</button>
</div>
{#if clickedButton == 'maps'}
	<Maps/>
{:else if clickedButton =='writing'}
	<Writing/>
{/if}
</div>