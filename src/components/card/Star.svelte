<script>
    import Icon from '@iconify/svelte';
    export let stars;
</script>

{#each stars as star}

<Icon icon="material-symbols:star" />
{/each}
