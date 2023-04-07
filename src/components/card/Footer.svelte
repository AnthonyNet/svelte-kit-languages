<script>
	export let props = props;
	export let handleClick = handleClick;
	const styles = {
		ul: 'flex  justify-around items-center',
		btn_div: 'flex flex-col border-t border-gray-300 text-gray-600',
		footer: ''
	};

	// your script goes here
	let switchState = false;
	console.log(props);

	function toggleSwitch() {
		switchState = !switchState;
	}
</script>

<footer class={styles.footer}>
	<div class="flex flex-row justify-around">
		<button on:click={toggleSwitch}>hint</button>

		<button on:click={handleClick}>click</button>
	</div>

	<ul class={styles.ul}>
		{#if switchState}
			<li>{props.base}</li>
			<li>{props.pastSimple}</li>
			<li>{props.pastParticiple}</li>
		{/if}
	</ul>
</footer>
