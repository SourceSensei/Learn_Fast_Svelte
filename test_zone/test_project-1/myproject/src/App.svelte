<script>
	let name = "Yoshi"
	let beltColor = "black"

	const handleClick = () => {
		beltColor = "orange"
	}

	const handleInput = (e) => {
		beltColor = e.target.value
	}

</script>

<main>
	<h1>Hello {name}!</h1>
	<!-- <p>{beltColor} belt</p> -->
	<p style="color: {beltColor}">{beltColor} belt</p>
	<!-- Events -->
	<button on:click={handleClick}>update belt color</button>
	<!-- <input type="text" on:input={handleInput} value={beltColor}> -->
	<input type="text" bind:value={beltColor}>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>