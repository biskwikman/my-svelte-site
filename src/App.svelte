<script>
	import Header from './components/Header.svelte';
	import Footer from './components/Footer.svelte';
	import Writing from './components/Writing.svelte';
	import Contact from './components/Contact.svelte';
	import Maps from './components/Maps.svelte'
	
	const unclickedBackgroundColor = 'white';
	const unclickedTextColor = '#526488';
	const clickedBackgroundColor = '#526488';
	const clickedTextColor = 'white';

	let clickedButton = '';

	function clickMaps() {
		clickedButton = 'maps-button';
		clickButton();
	}
	function clickWriting()	{
		clickedButton = 'writing-button';
		clickButton();
	}
	function clickContact() {
		clickedButton = 'contact-button';
		clickButton();
	}

	function clickButton() {
		const buttons = document.getElementsByClassName('title');
		for (let i = 0; i < buttons.length; i++) {
			if (buttons.item(i).id !== clickedButton) {
				buttons.item(i).style.backgroundColor = unclickedBackgroundColor
				buttons.item(i).style.color = unclickedTextColor
			}
			else {
				buttons.item(i).style.backgroundColor = clickedBackgroundColor
				buttons.item(i).style.color = clickedTextColor
			}
		}
	}
</script>

<div class="body">
	<Header/>
	<div class="main-buttons">
		<button class="title" id="maps-button" on:click={clickMaps}>Projects</button>
		<button class="title" id="writing-button" on:click={clickWriting}>Writing</button>
		<button class="title" id="contact-button" on:click={clickContact}>Contact</button>
	</div>
	{#if clickedButton === 'maps-button'}
		<Maps/>
	{:else if clickedButton === 'writing-button'}
		<Writing/>
	{:else if clickedButton === 'contact-button'}
		<Contact/>
	{/if}
	<Footer/>
</div>

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
		height: 3.5em;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	button:active {
		position: relative;
		top: 5px;
		left: 5px;
		box-shadow: 0px 0px 15px #526488;
	}
</style>
