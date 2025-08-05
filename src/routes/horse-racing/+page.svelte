<script>
	let horses = $state([
		{ emoji: '🦊', pos: 0, color: 'from-red-400 via-red-300 to-red-200' },
		{ emoji: '🐯', pos: 0, color: 'from-blue-400 via-blue-300 to-blue-200' },
		{ emoji: '🐴', pos: 0, color: 'from-green-400 via-green-300 to-green-200' },
		{ emoji: '🦄', pos: 0, color: 'from-purple-400 via-purple-300 to-purple-200' }
	]);

	const startRace = () => {
		horses.forEach((horse) => {
			horse.pos += Math.floor(Math.random() * 100 + 100);
		});
	};
</script>

<button class="my-5 border" onclick={startRace}>race start</button>

<div class="w-[600px] space-y-2">
	{#each horses as horse, index}
		<!-- lane {index + 1} -->
		<div class="p-2">
			<div class="relative mb-2 h-6 w-full overflow-hidden rounded bg-gray-200">
				<div
					class="h-full bg-gradient-to-r {horse.color} transition-all duration-1000"
					style="width: {Math.min(horse.pos / 6, 100)}%;"
				></div>
				<div class="absolute top-0 left-0 transition-all duration-1000" style="left: {horse.pos}px">
					{horse.emoji}
				</div>
			</div>
		</div>
	{/each}
</div>
