<script lang="ts">
	import Icon from '@iconify/svelte';
	import {onMount, onDestroy} from 'svelte';
	export let stars;



function log(){
	console.log(stars)
}

onMount(()=>{
	$: log()
})


</script>


	{#each stars as star}
	<Icon icon="material-symbols:star" />
{/each}
