<script lang="ts">
	import Star from '../card/Star.svelte';
	import Input from '../card/Input.svelte';

	import Footer from '../card/Footer.svelte';
	export let props;
/* ------------------------------------ */
/* SORT PROPS */
/* ------------------------------------ */
	const sortData = () => {
		const random = Math.floor(Math.random() * props.length);
		const data = props[random];
		return data;
	};

	let sorted = sortData();

	const score: number = 0;
	let stars: number[] | [] = [];

	const propsArray = [sorted.base, sorted.pastSimple, sorted.pastParticiple];

	const handleClick = () => {
		sorted = sortData();
		const el = document.querySelectorAll('.irrInput');
		el.forEach((item) => {
			item.classList.remove('text-green-500');
			item.classList.remove('text-red-500');
			item.value = '';
		});
	};

	/* ------------------------------------ */
	/* STYLES */
	/* ------------------------------------ */
	const styles = {
		section:
			'section_Responsive flex justify-center items-center w-full h-[91vh] responsiveSection',
		section_card:
			'min-w-[300px] p-4 h-auto card my-8 xl:my-0 border-4 border-double border-blue-700 rounded-lg shadow-xl shadow-slate-600 text-center',
		score_div: 'py-3  border-b border-gray-300',
		stars__div: 'flex items-center justify-center py-3 border-b border-gray-300 text-yellow-500',
		h5: 'text-xl dark:bg-black font-medium mb-2 border-b border-gray-300',
		ul: 'min-h-[150px] flex flex-col items-center justify-around',
	} as const;
</script>

<section class={styles.section}>
	<div class={styles.section_card}>
		<div class={styles.score_div}>
			Celkové skóre: <span>0</span>
		</div>
		<div class={styles.score_div}>
			Momentální skóre: <span>{score}</span>
		</div>

		<div class={styles.stars__div}>
			<Star />
		</div>

		<main>
			<h5 class={styles.h5}>{sorted.cz}</h5>

			<ul class={styles.ul}>
				{#each Object.entries(sorted) as [key, value]}
					{#if key !== 'cz'}
						<Input definition={key} props={value} />
					{/if}
				{/each}
			</ul>
		</main>

		<Footer handleClick={handleClick} props={sorted}/>
	</div>
</section>
