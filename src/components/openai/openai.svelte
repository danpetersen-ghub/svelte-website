<script>
	import { onMount } from 'svelte';

	/**
	 * @type {any}
	 */
	let response;

	async function getData() {
		try {
			const api = {
				baseURL: 'https://jsonplaceholder.typicode.com/todos/1',
				meta: {
					method: 'GET',
					headers: {
						'content-type': 'application/json',
						accept: 'application/json'
					}
				}
			};

			const res = await fetch(api.baseURL, api.meta);
			const json = await res.json();
			response = json;

			console.log(response);
		} catch (error) {
			console.error(error);
		}
	}

	console.log(response);
</script>

<div>
	<button on:click={getData}>Get Data</button>
</div>

<hr />

{#if response}
	<pre><code>{JSON.stringify(response, null, 2)}</code></pre>
{/if}
