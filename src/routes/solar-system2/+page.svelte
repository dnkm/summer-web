<div class="relative h-screen bg-gradient-to-b from-black via-gray-900 to-black">
	<!-- star -->
	<div
		class="absolute inset-1/2 h-14 w-14 -translate-1/2 animate-pulse rounded-full bg-yellow-300"
	></div>

	<!-- earth -->
	<div
		class="absolute inset-1/2 h-46 w-46 -translate-1/2 animate-[spin_16s_linear_infinite] rounded-full border border-gray-100/10"
	>
		<div
			class="absolute inset-4 h-4 w-4 animate-[spin_24s_linear_infinite] rounded-full bg-green-800 bg-gradient-to-b via-green-700 to-blue-600"
		>
			<div
				class="absolute -inset-1 h-1 w-1 rounded-full bg-yellow-50 bg-gradient-to-b via-yellow-100 to-yellow-200"
			></div>
		</div>
	</div>

	<!-- mercury -->
	<div
		class="absolute inset-1/2 h-30 w-30 -translate-1/2 animate-[spin_20s_linear_infinite] rounded-full border border-gray-100/10"
	>
		<div
			class="absolute inset-2.5 h-3 w-3 animate-[spin_24s_linear_infinite] rounded-full bg-red-800 bg-gradient-to-b via-yellow-700 to-red-600"
		></div>
	</div>

	<!-- random star -->
	{#each Array(200) as _, i}
		<div
			class="absolute h-0.5 w-0.5 animate-pulse rounded-full bg-white/40"
			style="top: {Math.random() * 95}vh; left: {Math.random() * 95}vw;"
		></div>
	{/each}
</div>
