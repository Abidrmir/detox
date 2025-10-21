<script>
	const phoneWeeks = 13 * 52;
	const pWeeks = Array.from({ length: phoneWeeks }, (_, i) => i);

	const sleepWeeks = 26 * 52;
	const sWeeks = Array.from({ length: sleepWeeks }, (_, i) => i);

	const livedWeeks = 41 * 52;
	const lWeeks = Array.from({ length: livedWeeks }, (_, i) => i);
</script>

<div class="snap-container">
	<!-- Section 1: Original Text -->
	<div class="snap-section flex h-screen items-center justify-center">
		<h1 class="text-center font-serif text-6xl font-extralight md:text-8xl lg:text-9xl">
			Scroll To See <br />
			<span class="italic underline decoration-emerald-600">Your Life</span>
		</h1>
	</div>

	<!-- Section 2: Image + Text Example -->
	<div class="snap-section flex h-screen justify-center overflow-hidden bg-gray-100 p-4">
		<div class="max-h-full md:overflow-y-auto">
			<h2 class="mb-2 text-center font-serif text-5xl md:text-8xl">Your Life in Weeks</h2>
			<div class="mb-3 flex items-center justify-center space-x-3 text-center font-serif text-sm md:text-2xl">
				<p class="font-bold text-black">Sleeping</p>
				<p class="font-bold text-red-400">Scrolling</p>
				<p class="font-bold text-emerald-700">Living</p>
			</div>
			<div class="space-y-5">
				<div class="grid grid-cols-60 gap-1 md:gap-1.5 md:grid-cols-100">
					{#each sWeeks as sWeek}
						<div class="h-1 w-1 rounded-full bg-black md:h-2 md:w-2"></div>
					{/each}
				</div>
				<div class="grid grid-cols-60 gap-1 md:grid-cols-100">
					{#each pWeeks as pWeek}
						<div class="h-1 w-1 rounded-full bg-red-400 md:h-2 md:w-2"></div>
					{/each}
				</div>
				<div class="grid grid-cols-60 gap-1 md:grid-cols-100">
					{#each lWeeks as lWeek}
						<div class="h-1 w-1 rounded-full bg-emerald-600 md:h-2 md:w-2"></div>
					{/each}
				</div>
			</div>
		</div>
	</div>

	<div class="snap-section flex h-screen items-center justify-center">
		<h1 class="text-center font-serif text-7xl font-extralight md:text-8xl lg:text-9xl">
			13 Years. <br />
			676 weeks. <br />
			<span class="italic underline decoration-red-400">Scrolling</span>
		</h1>
	</div>
	<!-- Add more sections here as needed -->
	<!-- Just copy the snap-section div structure and add your own content -->
</div>

<style>
	.snap-container {
		scroll-snap-type: y mandatory;
		overflow-y: scroll;
		height: 100vh;
	}

	.snap-section {
		scroll-snap-align: start;
		scroll-snap-stop: always;
	}
</style>
