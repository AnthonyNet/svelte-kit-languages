<script context="module">
	const style = {
		li: 'flex flex-col items-center',
		li_right: 'bg-green-500',
		input: 'border-2 py-1 text-center w-full font-extrabold irrInput',
		input_right: 'text-green-500',
		input_wrong: 'text-red-500'

	};
</script>

<script lang="ts">
	let score: number = 0;
	export let word: string = '';
	export let props: string;
	export let definition: string = '';


	function handleChange(e) {
		if (props.startsWith(word)) {

		}

	}
</script>

<li class={word === props ? style.li + ' ' + style.li_right : style.li}>
	<input
		type="text"
		class={props.startsWith(word)? style.input + ' ' + style.input_right : style.input+' '+style.input_wrong}
		placeholder={definition}
		bind:value={word}
		readonly={word === props ? true : false}
		on:input={handleChange}
	/>
</li>
