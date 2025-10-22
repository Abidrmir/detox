<script>
	const phoneWeeks = 13 * 52;
	const pWeeks = Array.from({ length: phoneWeeks }, (_, i) => i);

	const sleepWeeks = 26 * 52;
	const sWeeks = Array.from({ length: sleepWeeks }, (_, i) => i);

	const livedWeeks = 41 * 52;
	const lWeeks = Array.from({ length: livedWeeks }, (_, i) => i);

    import mainVideo from '$lib/videos/main.mp4';
    import vid2 from '$lib/videos/vid2.mp4'
    import vid3 from '$lib/videos/vid3.mp4'
    import vid4 from '$lib/videos/vid4.mp4'
    import vid5 from '$lib/videos/vid5.mp4'

    const videos = [mainVideo, vid2, vid3, vid4, vid5];

    const randomVideo = videos[Math.floor(Math.random() * videos.length)];

</script>

<div class="snap-container">
    <div class="snap-section flex h-screen items-center justify-center bg-cyan-200">
        <div class="relative w-full max-w-6xl px-4">
            <video 
            class="w-full rounded-lg shadow-2xl"
            controls
            autoplay
            muted
            playsinline
            src={randomVideo}
        >
            Your browser does not support the video tag.
        </video>
        </div>
    </div>

    <div class="snap-section flex h-screen justify-center bg-gray-200">
        <div class="flex flex-col text-center space-y-10">
            <h1 class="font-serif text-5xl mt-5">
                Answer The Folloing Quiz To See Full Video
            </h1>
            <p class="text-8xl">5 x 23 =</p>
        </div>
	</div>

	<div class="snap-section flex h-screen items-center justify-center">
		<h1 class="text-center font-serif text-6xl md:text-8xl lg:text-9xl">
			Scroll To See <br />
			<span class="italic underline decoration-emerald-600">Your Life</span>
		</h1>
	</div>

	<div class="snap-section flex h-screen justify-center overflow-hidden bg-gray-100 p-4">
		<div class="max-h-full md:overflow-y-auto">
			<h2 class="mb-2 text-center font-serif text-4xl md:text-8xl">Your Life in Weeks</h2>
			<div class="mb-3 flex items-center justify-center space-x-3 text-center font-serif text-sm md:text-2xl">
				<p class="font-bold text-black">Sleeping</p>
				<p class="font-bold text-red-400">Scrolling</p>
				<p class="font-bold text-emerald-700">Living</p>
			</div>
			<div class="space-y-3">
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
		<h1 class="text-center font-serif text-7xl md:text-8xl lg:text-9xl">
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
