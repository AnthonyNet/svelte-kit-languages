<script lang="ts">
    import Icon from '@iconify/svelte';
    export let stars: number[] | [] = [0];

</script>

{#each stars as star}

<Icon icon="material-symbols:star" />
{/each}
