<script context="module" lang="ts">
	const style = {
		li: 'flex flex-col items-center w-full',
		li_right: 'border-green-500 border-2',
		input: 'border-2 py-1 text-center w-full font-extrabold irrInput',
		input_right: 'text-green-500',
		input_wrong: 'text-red-500'
	};
</script>

<script lang="ts">
	export let word: string = '';
	export let props: string;
	export let definition: string = '';
	export let score: number;
	let currentScore = localStorage.getItem('totalScore');
	currentScore = currentScore ? parseInt(currentScore) : 0;
	localStorage.setItem('totalScore', currentScore);
</script>

<li class={word === props ? style.li + ' ' + style.li_right : style.li}>
	<input
		type="text"
		class={props.startsWith(word)
			? style.input + ' ' + style.input_right
			: style.input + ' ' + style.input_wrong}
		placeholder={definition}
		bind:value={word}
		readonly={word === props ? true : false}
		on:change={(e) => {
			if (e.target.value === props) {
				score++;
				localStorage.setItem('totalScore', (Number(currentScore) + 1).toString());
				currentScore = localStorage.getItem('totalScore');
			}
		}}
	/>
</li>
