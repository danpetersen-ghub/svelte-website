<script lang="ts">
	let navLinks: { name: string; url: string }[] = [
		{ name: 'Home', url: '/' },
		{ name: 'About', url: '/about' }
		// { name: 'Contact', url: '/contact' }
	];
</script>

<footer>
	<ul class="nav">
		{#each navLinks as link}
			<li><a href={link.url}>{link.name}</a></li>
		{/each}
	</ul>
</footer>

<style>
	footer,
	ul,
	li {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 20px;
		background-color: #e3e3e3;
		color: #fff;
		margin: 50px 0px;
		border-radius: 10px;
		text-decoration: none;
		text-align: center;
	}

	ul {
		text-align: center;
		min-width: 50%;
		margin: 0% 25%;
	}
</style>
