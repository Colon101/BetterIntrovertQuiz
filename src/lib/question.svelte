<script lang="ts">
	export let question: string;
	import { result, gameIndex } from '$lib/gamestores';
</script>

<div class="h-screen">
	<div class="flex justify-center">
		<div class=" fixed top-5 text-center">
			<h1 class=" text-3xl font-semibold">{question}</h1>
		</div>
	</div>
	<div class="flex h-[clac(100vh-4.5rem)] flex-col items-center gap-3 pt-48">
		{#each Array.from({ length: 10 }, (_, i) => i + 1) as i}
			<button
				class=" flex h-[6vh] max-h-14 w-5/6 max-w-[1000px] cursor-pointer items-center rounded-md bg-gray-500 transition-all hover:scale-[1.03] hover:bg-slate-700"
				on:click={() => {
					gameIndex.update((x) => x + 1);
					result.update((x) => x + i);
				}}
			>
				<div class=" ml-4 h-[14px] w-[14px] border-[1px] border-black bg-gray-300"></div>
				<span class="ml-4">
					{i} {i === 1 ? 'Not true of me at all' : ''} {i === 10 ? 'Very true of me' : ''}</span
				>
			</button>
		{/each}
	</div>
</div>
