<script>
	// @ts-nocheck
</script>

<h1>Netlify Form</h1>
<hr />
<!-- <form name="netlify-form-example" method="POST" netlify-honeypot="bot-field" data-netlify="true">
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
</form> -->

<form
	name="dp-test-form"
	method="POST"
	data-netlify="true"
	netlify
	action="/success"
	style="background-color: forestgreen;border-radius: 5px "
>
	<input type="hidden" name="form-name" value="dp-test-form" />

	<label for="name">Name</label>
	<input name="name" id="name" required placeholder="Name" type="text" />
	<label for="email">Email</label>
	<input name="email" id="email" required placeholder="Email" type="email" />
	<label for="message">Message</label>
	<input name="message" id="message" required placeholder="Message" type="text" />
	<input
		type="submit"
		value="Submit"
		style="background-color: white; border-radius: 5px;margin-top: 20px;"
	/>
	<div netlify-recaptcha />
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
		width: 97%;
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
		max-width: 600px;
		margin: 0 auto;
		padding: 20px;
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
