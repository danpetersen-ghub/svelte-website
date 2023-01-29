<script>
// @ts-nocheck

	import Triple from './learningnested.svelte';
	import Dogs from './learninglogicblock.svelte';
	import Await from './learningAwaitBlock.svelte';
	
	let BoldString = `<strong> THIS IS A JS STRING </strong>`
	let count = 0;
	
	function handleClick() {count += 1; 	}
	
	/**
		 * @param {number} num
	*/
	function checkCount(num) {
	 if(num == 10){
		BoldString = `<strong> THIS IS A JS STRING - WOOO HOO CLICKED TEM TIMES </strong>`
	 }
	}

	// Don't worry if this looks a little alien. 
	// It's valid (if unconventional) JavaScript, which Svelte interprets to mean 
	// 're-run this code whenever any of the referenced values change'. 
	// Once you get used to it, there's no going back.
	$: doubled = count * 2;
	$: console.log('the count is ' + count);
	$: checkCount(count);

	let num = 123;

	</script>

<p>This is static HTML in a Component </p>
<p>{@html BoldString}</p>
<button on:click={handleClick}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>
<br>
<i>count times 2 = {doubled}</i>

<Triple data={num}/>
<Await></Await>
<Dogs />

<style>
	p {
		color: purple;
		font-size: 12px;	
	}
</style>

