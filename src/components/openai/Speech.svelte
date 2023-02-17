<script>
	import { Configuration, OpenAIApi } from 'openai';

	let text = 'activated';

	function onMount() {
		const configuration = new Configuration({
			organization: 'org-3hFrcqV54ECg7Dq8XbFhIpR8',
			apiKey: process.env.OPENAI_API_KEY
		});
		const openai = new OpenAIApi(configuration);

		const synth = window.speechSynthesis;

		let data = {
			id: 'cmpl-GERzeJQ4lvqPk8SkZu4XMIuR',
			object: 'text_completion',
			created: new Date(),
			model: 'text-davinci:003',
			choices: [
				{
					text: text,
					index: 0,
					logprobs: null,
					finish_reason: 'length'
				}
			],
			usage: {
				prompt_tokens: 5,
				completion_tokens: 7,
				total_tokens: 12
			}
		};

		//const response = await openai.listEngines();
	}

	// /**
	//  * @param {{ preventDefault: () => void; }} event
	//  */
	function handleSubmit() {
		console.log('activated', text);
		// const utterThis = new SpeechSynthesisUtterance(text);
		// synth.speak(utterThis);
	}
</script>

<form on:submit|preventDefault={handleSubmit}>
	<input type="text" name="text" bind:value={text} />
	<button type="submit">Voice</button>
</form>

<p>{text}</p>
