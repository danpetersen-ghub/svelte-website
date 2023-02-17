<script>
	// @ts-nocheck
</script>

<h1>Netlify Form</h1>
<hr />
<form name="netlify-form-example" method="POST" netlify-honeypot="bot-field" data-netlify="true">
	<p>
		<label>Your Name: <input type="text" name="name" /></label>
	</p>
	<p>
		<label>Your Email: <input type="email" name="email" /></label>
	</p>
	<p>
		<label
			>Your Role: <select name="role[]" multiple>
				<option value="leader">Leader</option>
				<option value="follower">Follower</option>
			</select></label
		>
	</p>
	<p>
		<label>Message: <textarea name="message" /></label>
	</p>
	<p>
		<button type="submit">Send</button>
	</p>
</form>

<style>
	/* Add your styles here */
	label {
		display: block;
		margin-bottom: 10px;
	}

	input,
	textarea,
	select {
		width: 100%;
		padding: 10px;
		border-radius: 5px;
		border: 1px solid #ccc;
		font-size: 16px;
	}

	button {
		background-color: #4caf50;
		color: white;
		padding: 10px 20px;
		border-radius: 5px;
		border: none;
		cursor: pointer;
		font-size: 16px;
	}

	button:hover {
		background-color: #3e8e41;
	}

	form {
		max-width: 500px;
		margin: 0 auto;
	}

	h1 {
		text-align: center;
	}

	hr {
		margin-top: 20px;
		margin-bottom: 20px;
		border: 0;
		border-top: 1px solid #ccc;
	}
</style>
