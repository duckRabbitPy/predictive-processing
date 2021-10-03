<script>
	import Part1 from '$lib/Part1.svelte';
	import Part2 from '$lib/Part2.svelte';
	import Part3 from '$lib/Part3.svelte';
	import Part4 from '$lib/Part4.svelte';

	let options = [
		{ part: '1', value: 'Part 1: Introduction to predictive processing' },
		{ part: '2', value: 'Part 2: Bayesian inference' },
		{ part: '3', value: 'Part 3: The perceptual hierarchy' },
		{ part: '4', value: 'Part 4: Precision expectation and psychosis' }
	];

	let part = '1';

	let sources = {
		'1': 'https://www.youtube.com/embed/EIzuFpWaxnQ',
		'2': 'https://www.youtube.com/embed/9etQFjvknh8',
		'3': 'https://www.youtube.com/embed/eTYR4MjK8cc',
		'4': 'https://www.youtube.com/embed/8DUMH5qMvQE'
	};
</script>

<h1>Predictive processing video series</h1>
<select bind:value={part}>
	{#each options as option}
		<option value={option.part}>{option.value}</option>
	{/each}
</select>

<div class="vid-transcript">
	<iframe
		src={sources[part]}
		title="YouTube video player"
		frameborder="0"
		allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
		allowfullscreen
	/>
	{#if part === '1'}
		<Part1 />
	{/if}

	{#if part === '2'}
		<Part2 />
	{/if}

	{#if part === '3'}
		<Part3 />
	{/if}

	{#if part === '4'}
		<Part4 />
	{/if}
</div>

<style>
	h1,
	h2,
	h3,
	h4,
	h5,
	p,
	a {
		margin-left: 2.5rem;
	}

	iframe {
		margin-top: 1rem;
		height: 70vh;
		width: 70vw;
	}

	select {
		font-size: large;
		margin-left: 2.5rem;
	}

	.vid-transcript {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-left: 2.5rem;
		margin-right: 2.5rem;
	}
</style>
