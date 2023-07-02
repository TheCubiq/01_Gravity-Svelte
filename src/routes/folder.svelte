<script>
	import { createEventDispatcher, onMount } from 'svelte';
	import { afterUpdate } from 'svelte';

	const dispatch = createEventDispatcher();

	let isOpen = false;

	function toggleFolder() {
		isOpen = !isOpen;
		dispatch('toggle', isOpen);
	}

	
</script>

<div aria-hidden="true" class="folder" class:isOpen id="folder" on:click={toggleFolder}>
	<div class="folder-icon">📁</div>
	<div class="folder-name">Folder</div>
</div>

{#if isOpen}
	<div class="file-list">
		<slot />
	</div>
{/if}

<style lang="stylus" type="text/stylus">
	itemColor = hsl(212, 75%, 58%)
	// @import '../styles/folder.styl'
	@require '../styles/folder.styl'
	
</style>
