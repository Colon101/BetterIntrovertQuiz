<script lang="ts">
	export let question: string;
	import { result, gameIndex } from '$lib/gamestores';
</script>

<div class="flex justify-center pb-12 pt-6">
	<h1 class="text-center text-3xl font-semibold">{question}</h1>
</div>
<div class="flex flex-col items-center gap-3">
	{#each [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] as i}
		<button
			class=" flex h-[5vh] max-h-14 w-5/6 max-w-[1000px] cursor-pointer items-center rounded-md bg-gray-500 transition-all hover:scale-[1.03] hover:bg-slate-700"
			on:click={() => {
				gameIndex.update((x) => x + 1);
				result.update((x) => x + i);
			}}
		>
			<span class="ml-4">
				{i} {i === 1 ? 'Not true of me at all' : ''} {i === 10 ? 'Very true of me' : ''}</span
			>
		</button>
	{/each}
</div>
