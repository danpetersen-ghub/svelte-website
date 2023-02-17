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
	INPUT {
		color: #000;
		width: 100%;
	}
</style>
