<script>
	let dogImg = $state('');

	function loadDogImg() {
		fetch('https://dog.ceo/api/breeds/image/random')
			.then((v) => v.json())
			.then((v) => (dogImg = v.message));
	}

	let trivia = $state([]);

	async function loadProblem() {
		let res = await fetch(
			'https://opentdb.com/api.php?amount=2&category=12&difficulty=easy&type=boolean'
		);
		let data = await res.json();
		console.log(data);
		trivia = data.results;
	}

	let games = $state(null);
	async function loadGames() {
		0d67b63cc19540ccbfa5cd358eb70bf8
	}
</script>

<div class="prose">
	<h1>Random Dog Images</h1>
	<img src={dogImg} width="400" alt="dog" onclick={loadDogImg} />

	<h1>trivia</h1>
	<button onclick={loadProblem}>load</button>
	{#each trivia as q, i}
		<div class="flex border rounded p-4">
      <div>{q.type}</div>
      <div>{q.difficulty}</div>
      <div>{q.category}</div>
      <div>{q.question}</div>
    </div>
	{/each}
</div>
