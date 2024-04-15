<script lang="ts">
	export let question: string;
	export let result: number;
	export let questionNum: number;
</script>

<div class="flex justify-center py-12">
	<h1 class="text-4xl text-center">{question}</h1>
</div>
<div class="flex flex-col items-center gap-3">
	{#each [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] as i}
		<button
			class=" rounded-md cursor-pointer max-w-[1000px] w-5/6 h-14 bg-gray-500 hover:bg-slate-700 hover:scale-[1.03] transition-all flex items-center"
			on:click={() => {
				questionNum += 1;
				result += i;
			}}
		>
			<span class="ml-4">
				{i} {i === 1 ? 'Not true of me at all' : ''} {i === 10 ? 'Very true of me' : ''}</span
			>
		</button>
	{/each}
</div>
