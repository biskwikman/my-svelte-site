<script>
	import Header from './components/Header.svelte';
	import Writing from './components/Writing.svelte';
	import Maps from './components/Maps.svelte'
	
	let clickedButton = '';

	function clickMaps() {
		clickedButton = 'maps';
		document.getElementById('maps-button').style.backgroundColor = '#526488';
		document.getElementById('maps-button').style.color = 'white';
		document.getElementById('writing-button').style.backgroundColor = 'white';
		document.getElementById('writing-button').style.color = '#526488';
	}
	function clickWriting()	{
		clickedButton = 'writing';
		document.getElementById('maps-button').style.backgroundColor = 'white';
		document.getElementById('maps-button').style.color = '#526488';
		document.getElementById('writing-button').style.backgroundColor = '#526488';
		document.getElementById('writing-button').style.color = 'white';
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
		border: 2px solid gray;
		background: none;
		border-radius: 5px;
		box-shadow: 2px 2px 10px #526488;
		cursor: pointer;
		width: calc(4em + 1vw);
	}

	button:active {
		position: relative;
		top: 5px;
		left: 5px;
		box-shadow: 0px 0px 15px #526488;
	}
</style>
<Header/>

<div>
<div class="main-buttons">
	<button class="title" id="maps-button" on:click={clickMaps}>Maps <br> 地図</button>
	<button class="title" id="writing-button" on:click={clickWriting}>Writing <br> 文章</button>
</div>
{#if clickedButton == 'maps'}
	<Maps/>
{:else if clickedButton =='writing'}
	<Writing/>
{/if}
</div>