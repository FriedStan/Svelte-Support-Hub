<script lang="ts">
	import './layout.css';
	import icon from '$lib/assets/img/it-logo.png';
	import { ModeWatcher } from "mode-watcher";
	import Header from '$lib/Header.svelte';
	
	let { children } = $props();
</script>

<Header></Header>

<svelte:head>
	<title>หน้าหลัก | ITSupportHub</title>
	<link rel="icon" href={icon} />
</svelte:head>

<ModeWatcher />
{@render children()}
