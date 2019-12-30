<script>
	import Header from './components/Header.svelte';
	import Footer from './components/Footer.svelte';
	import Writing from './components/Writing.svelte';
	import Contact from './components/Contact.svelte';
	import Maps from './components/Maps.svelte'
	
	let clickedButton = '';

	function clickMaps() {
		clickedButton = 'maps';
		document.getElementById('maps-button').style.backgroundColor = '#526488';
		document.getElementById('maps-button').style.color = 'white';
		document.getElementById('writing-button').style.backgroundColor = 'white';
		document.getElementById('writing-button').style.color = '#526488';
		document.getElementById('contact-button').style.backgroundColor = 'white';
		document.getElementById('contact-button').style.color = '#526488';
	}
	function clickWriting()	{
		clickedButton = 'writing';
		document.getElementById('maps-button').style.backgroundColor = 'white';
		document.getElementById('maps-button').style.color = '#526488';
		document.getElementById('writing-button').style.backgroundColor = '#526488';
		document.getElementById('writing-button').style.color = 'white';
		document.getElementById('contact-button').style.backgroundColor = 'white';
		document.getElementById('contact-button').style.color = '#526488';
	}
	function clickContact() {
		clickedButton = 'contact';
		document.getElementById('maps-button').style.backgroundColor = 'white';
		document.getElementById('maps-button').style.color = '#526488';
		document.getElementById('writing-button').style.backgroundColor = 'white';
		document.getElementById('writing-button').style.color = '#526488';
		document.getElementById('contact-button').style.backgroundColor = '#526488';
		document.getElementById('contact-button').style.color = 'white';
	}
</script>

<style>

	.body {
		display: flex;
		flex-direction: column;
		height: 100%;
	}

	.main-buttons {
		flex: 1 0 auto;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		text-align: center;
		align-items: flex-start;
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

<div class="body">
	<Header/>
	<div class="main-buttons">
		<button class="title" id="maps-button" on:click={clickMaps}>Maps <br> 地図</button>
		<button class="title" id="writing-button" on:click={clickWriting}>Writing <br> 文章</button>
		<button class="title" id="contact-button" on:click={clickContact}>Contact <br> 連絡</button>
	</div>
	{#if clickedButton == 'maps'}
		<Maps/>
	{:else if clickedButton == 'writing'}
		<Writing/>
	{:else if clickedButton == 'contact'}
		<Contact/>
	{/if}
	<Footer/>
</div>