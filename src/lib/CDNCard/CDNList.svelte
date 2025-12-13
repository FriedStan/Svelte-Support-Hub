<script lang="ts">
	import { flip } from 'svelte/animate';
	import { send, receive } from './transition.ts';

	let { cdn } = $props();
</script>

<ul>
	{#each cdn as item (item.id)}
		<li
			class={{ done: item.done }}
			in:receive={{ key: item.id }}
			out:send={{ key: item.id }}
			animate:flip={{ duration: 200 }}
		>
			<label>
				<input type="checkbox" bind:checked={item.done}/>
				<span class="ml-2 break-all">{item.description}</span>
			</label>
		</li>
	{/each}
</ul>

<style>
	label {
		width: 100%;
		height: 100%;
		display: flex;
	}

	span {
		flex: 1;
	}
</style>
