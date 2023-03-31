<script>
	const style = {
		button:
			'px-6 py-2.5 mt-2 mb-2 bg-blue-800 text-white font-medium text-xs leading-tight uppercase rounded shadow-md hover:bg-indigo-700 hover:shadow-lg focus:bg-blue-700 focus:shadow-lg focus:outline-none focus:ring-0 active:bg-blue-800 active:shadow-lg transition duration-150 ease-in-out',
		ul: 'flex  justify-around items-center'
	};

	let props = {
		base: 'base',
		pastSimple: 'pastSimple',
		pastParticiple: 'pastParticiple'
	};
	// your script goes here
	let switchState = false;
	console.log(switchState);
	function toggleSwitch() {
		switchState = !switchState;
	}
</script>

<div>
	<button class={style.button} on:click={toggleSwitch}>hint</button>
	<ul class={style.ul}>
		{#if switchState}
			<li>{props.base}</li>
			<li>{props.pastSimple}</li>
			<li>{props.pastParticiple}</li>
		{/if}
	</ul>
</div>
