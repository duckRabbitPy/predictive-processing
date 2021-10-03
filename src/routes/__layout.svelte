<script>
	// import global css from src
	import MenuButton from '$lib/MenuButton.svelte';
	import '/src/global.css';
	import Footer from '/src/lib/Footer.svelte';
</script>

<nav>
	<ul>
		<MenuButton link=".">Main</MenuButton>
		<MenuButton link="about">About</MenuButton>
		<MenuButton link="videos">My videos</MenuButton>
		<MenuButton link="resources">Resources</MenuButton>
		<MenuButton link="notes">Reading Notes</MenuButton>
	</ul>
</nav>

<slot />

<Footer />

<style>
	button {
		background-color: darkcyan;
	}

	a {
		color: white;
		padding: 1rem;
	}
</style>
