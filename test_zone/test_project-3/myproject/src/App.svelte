<script>
	let people = [
		{ name : 'yoshi', beltColor: 'black', age: 25, id: 1},
		{ name : 'mario', beltColor: 'orange', age: 45, id: 2},
		{ name : 'luigi', beltColor: 'brown', age: 35, id: 3}
	]

	const handleClick = (id) => {
		//delete the person from people
		people = people.filter((person) => person.id != id)
	}

	//Conditionals
	let num = 5
</script>

<!-- Conditionals -->
{#if num > 20}
	<p>Greater than 20</p>
{:else if num > 5}
 	<p>Greater than 5</p>
{:else}
	<p>Not greater than 5</p>
{/if}

<main>
	<!-- Loops -->
	<!-- Adding an id is a good practice -->
	{#each people as person (person.id)}
		<div>
			<h4>{person.name}</h4>
			<p>{person.age} years old, {person.beltColor} belt.</p>
			<button on:click={() => handleClick(person.id)}>delete</button>
		</div>
	{:else}
		<p>There are no people to show...</p>
	{/each}
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