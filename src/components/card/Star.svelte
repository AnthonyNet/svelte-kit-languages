<script>
    import Icon from '@iconify/svelte';
    let stars = [0,0];
</script>

{#each stars as star}
	
<Icon icon="material-symbols:star" />
{/each}
