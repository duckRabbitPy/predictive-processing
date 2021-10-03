<script>
	import Hoverable from '/src/lib/Hoverable.svelte';
	import { fade } from 'svelte/transition';
	import GlitchHeader from '$lib/GlitchHeader.svelte';
</script>

<div class="container">
	<div>
		<GlitchHeader />
	</div>

	<div class="quote">
		<Hoverable let:hovering={active}>
			<div class:active>
				<div class="graphic">
					<img class="graphic" src="/brain.svg" alt="brain graphic" />
				</div>
				{#if active}
					<h3 transition:fade>“Perception is a controlled hallucination.” - Andy Clark</h3>
				{/if}
			</div>
		</Hoverable>
	</div>

	<div class="quote">
		<Hoverable let:hovering={active}>
			<div class:active>
				<div class="graphic">
					<img class="graphic" src="/cord.svg" alt="spinal cord graphic" />
				</div>
				{#if active}
					<h3 transition:fade>
						“Learning and perception are two sides of the same coin” - Karl Friston
					</h3>
				{/if}
			</div>
		</Hoverable>
	</div>

	<div class="quote">
		<Hoverable let:hovering={active}>
			<div class:active>
				<div class="graphic">
					<img class="graphic" src="/brain2.svg" alt="brain graphic" />
				</div>
				{#if active}
					<h3 transition:fade>
						“Conscious perception is determined by the hypothesis that best minimises prediction
						error” - Jakob Howhy
					</h3>
				{/if}
			</div>
		</Hoverable>
	</div>

	<div class="quote">
		<Hoverable let:hovering={active}>
			<div class:active>
				<div class="graphic">
					<img class="graphic" src="/body.svg" alt="body graphic" />
				</div>
				{#if active}
					<h3 transition:fade>
						“Movement ensues when the sensory consequences of an action are strongly predicted." -
						Andy Clark
					</h3>
				{/if}
			</div>
		</Hoverable>
	</div>
</div>

<style>
	h3 {
		margin-left: 2.5rem;
		font-family: 'Open Sans';
		font-weight: 200;
	}

	.quote {
		display: flex;
		flex-direction: row;
		justify-content: center;
		padding-bottom: 2rem;
	}

	.container {
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.graphic {
		display: flex;
		flex-direction: row;
		justify-content: center;
		height: 400px;
	}

	.graphic:hover {
		opacity: 70%;
	}
</style>
