<script>
	let text = 'Welcome to my very silly App!';

	async function handleSubmit() {
		console.log('submit');

		const synth = window.speechSynthesis;

		let voices = await synth.getVoices();

		console.log('voices is:', voices[0]);

		const utterThis = new SpeechSynthesisUtterance(text);

		utterThis.voice = voices[0];

		utterThis.rate = 0.9;

		utterThis.pitch = 1.2;

		synth.speak(utterThis);
	}
</script>

<form on:submit|preventDefault={handleSubmit}>
	<input bind:value={text} type="text" />
	<button type="submit">Activate</button>
</form>

<style>
	form {
		display: flex;
		flex-direction: row;
		align-items: center;
	}

	input[type='text'] {
		flex: 1;
		margin-right: 10px;
		padding: 10px;
		font-size: 16px;
		border: 2px solid #ccc;
		border-radius: 5px;
	}

	button[type='submit'] {
		padding: 10px;
		font-size: 16px;
		background-color: #4caf50;
		color: white;
		border: none;
		border-radius: 5px;
		cursor: pointer;
	}
</style>
