<script>
    import { onMount } from 'svelte';
    /**
	 * @type {any}
	 */
    let response;
    async function getData() {
        // Make the API Call here
        const api = {
            baseURL:'https://jsonplaceholder.typicode.com/todos/1',
            meta: {
                headers: {
                    "Method": "GET",
                    "Content-Type": "application/json",
                    "Accept": "application/json",
                    "Access-Control-Allow-Origin": "*",
                    }
                }
        }
        return response = await fetch(`${api.baseURL}`, api.meta);
    }
</script>
<div>
    <button on:click={getData}>Get Data</button>
</div>

<hr>

{#if response }

<pre><code>
    {response.id}
</code></pre>

{/if}