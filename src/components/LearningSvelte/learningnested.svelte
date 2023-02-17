<h5>
    nested tripple count is { tripple }
</h5>

{#if tripple > 300}
	<p>{tripple} is greater than 300</p>
{:else}
	{#if 123 > tripple}
		<p>{tripple} is less than 123</p>
	{:else}
		<p>{tripple} is between 123 and 300</p>
	{/if}
{/if}

<script>
 export let data;

let tripple = data * 3
</script>