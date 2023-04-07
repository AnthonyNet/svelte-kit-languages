<script>
	import { onMount } from 'svelte';
	import { writable } from 'svelte/store';

	const totalScore = writable(0);

	onMount(() => {
		const storedScore = localStorage.getItem('totalScore');
		if (storedScore) {
			totalScore.set(parseInt(storedScore));
		} else {
			localStorage.setItem('totalScore', '0');
		}
	});
	// check the function increaseScore and fix the error

	function increaseScore() {
		totalScore.update((score) => score + 1);
		localStorage.setItem('totalScore', totalScore.toString());
	}
</script>

<span>{$totalScore}</span>

<button on:click={increaseScore}>Increase Score</button>
