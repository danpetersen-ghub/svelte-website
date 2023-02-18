<script lang="ts">
	import { onMount } from 'svelte';

	let showNav = false;
	const toggleNav = (): void => {
		showNav = !showNav;
	};

	onMount(() => {
		document.addEventListener('click', (event: Event) => {
			const target = event.target as HTMLElement;
			if (!target.closest('.nav') && showNav) {
				showNav = false;
			}
		});
	});
</script>

<header>
	<!-- <button class="nav-toggle" on:click={toggleNav}>
		<span />
		<span />
		<span />
	</button> -->
	<nav>
		<a href="/about">about</a>
		<a href="/learning-svelte">learning-svelte</a>
		<a href="/openai">openai</a>
		<a href="/speech">speech</a>
		<a href="/netlify-form">netlify-form</a>
		<a href="/netlify-identity">netlify-identity</a>
	</nav>
</header>

<style>
	header {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 20px;
		background-color: firebrick;
		border-radius: 10px;
	}

	.nav {
		border-radius: 25%;
		display: flex;
		flex-direction: column;
		position: absolute;
		top: 100%;
		left: 0;
		right: 0;
		background-color: #fff;
		padding: 20px;
		transform: translateY(-100%);
		transition: transform 0.3s ease-in-out;
		z-index: 1;
	}

	.nav a {
		display: block;
		padding: 10px 10px;
		color: #fff;
		text-decoration: none;
		font-weight: bold;
	}
	a {
		color: #fff;
		/* text-decoration: none; */
		font-weight: bold;
		padding: 10px 10px;
	}
</style>
