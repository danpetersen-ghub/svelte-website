<script>
	export let message = 'Form submitted successfully!';
	import NavBar from '../../components/NavBar.svelte';
	import Footer from '../../components/Footer.svelte';
</script>

<NavBar />

<div>
	<div class="container">
		<div class="success-icon">
			<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
				<path
					fill="#00b300"
					d="M12 0c-6.628 0-12 5.372-12 12s5.372 12 12 12 12-5.372 12-12-5.372-12-12-12zm4.293 9.707l-6.293 6.293-2.293-2.293-1.414 1.414 3 3 .707.707.707-.707 7-7-1.414-1.414z"
				/>
			</svg>
		</div>
		<p class="message">{message}</p>
	</div>
</div>

<Footer />

<style>
	.container {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		height: 100vh;
		background-color: #fff;
	}

	.success-icon {
		width: 100px;
		height: 100px;
		display: flex;
		justify-content: center;
		align-items: center;
		border-radius: 50%;
		background-color: #ffffff;
	}

	.success-icon svg {
		width: 50%;
	}
</style>
