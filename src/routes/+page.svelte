<script lang="ts">
	import Question from '$lib/question.svelte';
	let result = 0;
	let questionIndex = 0;
</script>

<div class="pb-3">
	{#if questionIndex === 0}
		<Question
			question={'1. I enjoy spending time in solitude.'}
			bind:result
			bind:questionNum={questionIndex}
		/>
	{/if}
	{#if questionIndex === 1}
		<Question
			question={'2. I prefer for someone else to be the center of attention.'}
			bind:result
			bind:questionNum={questionIndex}
		/>
	{/if}
	{#if questionIndex === 2}
		<Question
			question={'3. I prefer spending time one-on-one with others rather than hanging out in a group.'}
			bind:result
			bind:questionNum={questionIndex}
		/>
	{/if}
	{#if questionIndex === 3}
		<Question
			question={'4. I listen and think before I speak.'}
			bind:result
			bind:questionNum={questionIndex}
		/>
	{/if}
	{#if questionIndex === 4}
		<Question
			question={'5. I need time to process before making decisions.'}
			bind:result
			bind:questionNum={questionIndex}
		/>
	{/if}
	{#if questionIndex === 5}
		<Question
			question={'6. I’m drawn to deep conversations and thoughts.'}
			bind:result
			bind:questionNum={questionIndex}
		/>
	{/if}
	{#if questionIndex === 6}
		<Question
			question={'7. I need time alone to recharge and reflect.'}
			bind:result
			bind:questionNum={questionIndex}
		/>
	{/if}
	{#if questionIndex === 7}
		<Question
			question={'8. I’m observant and often notice what others miss.'}
			bind:result
			bind:questionNum={questionIndex}
		/>
	{/if}
	{#if questionIndex === 8}
		<Question
			question={'9. I prefer working in quiet, independent environments.'}
			bind:result
			bind:questionNum={questionIndex}
		/>
	{/if}
	{#if questionIndex === 9}
		<Question
			question={'10. I’m at my best when I fully focus rather than divide my attention.'}
			bind:result
			bind:questionNum={questionIndex}
		/>
	{/if}
	{#if questionIndex > 9}
		<h1 class="text-4xl text-center font-semibold">Your result: {result}/100</h1>
	{/if}
</div>
