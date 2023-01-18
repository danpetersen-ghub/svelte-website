<script>
// @ts-nocheck
    let number

    let myPromise = new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve(
                number = getRandomNumber(1,1000)
            );
        }, 5000);
    });

    myPromise.then((successMessage) => {
        console.log(successMessage);
    });

    function getRandomNumber(min, max) {
        return Math.floor(Math.random() * (max - min + 1)) + min;
    }

</script>

{#await myPromise}
	<p>...waiting random number...</p>
{:then number}
	<p>The number is {number}</p>
{:catch error}
	<p style="color: red">{error.message}</p>
{/await}