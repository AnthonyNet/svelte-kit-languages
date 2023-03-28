<script lang="ts">
	import Star from '../card/Star.svelte';
    import Input from '../card/Input.svelte';

	export let myData: any;

	const score = 0;
	let stars:number[]|[] = [];

	const randomNumber = Math.floor(Math.random() * myData.length);
	/*------------------------------------------
    Props Data from Object to Array
         + first item deleted from Array
       -------------------------------------------*/
    const propertyValues = Object.values(myData[randomNumber]);
	const cz = myData[randomNumber].cz;
    propertyValues.shift();
	const reverseArray = propertyValues.reverse();


    const styles = {
		section:
			'section_Responsive flex justify-center items-center w-full h-[91vh] responsiveSection',
		section_div:
			'max-w-sm card my-8 xl:my-0 border-4 border-double border-blue-700 rounded-lg shadow-xl shadow-slate-600 text-center',
		score_div: 'py-3 px-6 border-b border-gray-300',
		stars__div: 'flex items-center justify-center py-3 border-b border-gray-300 text-yellow-500',
		btn_div: 'border-t border-gray-300 text-gray-600',
		h5: 'text-xl dark:bg-black font-medium mb-2 border-b border-gray-300',
		ul: 'flex flex-col items-center relative h-[100px]'
	} as const;
</script>

<section class={styles.section}>
	<div class={styles.section_div}>

		<div class={styles.score_div}>
			Celkové skóre: <span>0</span>
		</div>
		<div class={styles.score_div}>
			Momentální skóre: <span>{score}</span>
		</div>

		<div class={styles.stars__div}>

				<Star />

		</div>

		<div class="px-6">
			<h5 class={styles.h5}>{cz}</h5>

			<ul class={styles.ul} >

				{#each reverseArray as props}

					<Input props={props}  />
				{/each}
			</ul>

			<div class={styles.btn_div}>
				<button />
			</div>
		</div>

		<div class={styles.btn_div}>
			<button />

			hints
		</div>
	</div>
</section>
