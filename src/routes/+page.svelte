<script lang="ts">
	import Question from '$lib/question.svelte';
	import { gameIndex, result } from '$lib/gamestores';
	const questions = [
		'1. I enjoy spending time in solitude.',
		'2. I prefer for someone else to be the center of attention.',
		'3. I prefer spending time one-on-one with others rather than hanging out in a group.',
		'4. I listen and think before I speak.',
		'5. I need time to process before making decisions.',
		'6. I’m drawn to deep conversations and thoughts.',
		'7. I need time alone to recharge and reflect.',
		'8. I’m observant and often notice what others miss.',
		'9. I prefer working in quiet, independent environments.',
		'10. I’m at my best when I fully focus rather than divide my attention.'
	];
</script>

{#each questions as question, i}
	{#if $gameIndex === i}
		<Question {question} />
	{/if}
{/each}

{#if $gameIndex >= questions.length}
	<h1 class="text-center text-4xl font-semibold">Your result: {$result}/100</h1>
	<div class=" flex h-[50vh] items-center justify-center">
		<button
			class="rounded-lg bg-purple-700 px-5 py-2.5 text-center text-sm font-medium text-white transition-all hover:-translate-y-2 hover:bg-purple-800 focus:outline-none focus:ring-4 focus:ring-purple-300 dark:bg-purple-600 dark:hover:bg-purple-700 dark:focus:ring-purple-800"
			on:click={() => {
				gameIndex.set(0);
				result.set(0);
			}}>Restart</button
		>
	</div>
{/if}
