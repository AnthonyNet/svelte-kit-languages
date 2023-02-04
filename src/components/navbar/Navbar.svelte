<script>
	import NavbarMobile from './Navbar_mobile.svelte';
  import {IrregularVerbs, OxfordB1, OxfordB2, OxfordC1, LukesPhrasal, VerbenData, Goethe } from '../../myData/';


	const styles = {
		nav: 'flex justify-center items-center w-full  min-h-[100px] shadow-xl z-[400] px-4',
		nav__div: 'navDetails   w-full h-full flex items-start  relative text-xl ',
		aside: 'logo sm:w-1/3 ',
		article: 'justify-around items-start w-full h-full hidden md:flex',
		nav__ul: 'hidden flex flex-col border-solid border-t-4 border-sky-400 navDetails'
	};


</script>

<nav class={styles.nav}>
	<div class={styles.nav__div}>
		<aside class={styles.aside}>
			<a href="/">
				Learn <strong>languages</strong>
			</a>
		</aside>
		<article class={styles.article}>
			<a href="/">Home</a>
			<details class="cursor-pointer">
				<summary class="uppercase logo">
					<strong class="hover:text-sky-700">English</strong>
				</summary>
				<div class="flex flex-col border-solid border-t-4 border-sky-400 navDetails">
					<a href="/english/irregular-verbs">{`Irregular Verbs (${IrregularVerbs.length})`}</a>
					<a href="/english/search-irregular">{`Irregular List (${IrregularVerbs.length})`}</a>
					<a href="/english/oxford-B1">{`Oxford B1 (${OxfordB1.length})`}</a>
					<a href="/english/oxford-B2">{`Oxford B2 (${OxfordB2.length})`}</a>
					<a href="/english/oxford-C1">{`Oxford C1 (${OxfordC1.length})`}</a>
					<a href="/english/phrasal-verbs">{`Phrasal Verbs (${LukesPhrasal.length})`}</a>
					<a href="/english/pagination">Pagination</a>
				</div>
			</details>

			<details class="cursor-pointer">
				<summary class="uppercase logo">
					<strong class="hover:text-sky-700">Deutsch</strong>
				</summary>
				<ul class="flex flex-col border-solid border-t-4 border-sky-400 navDetails">
					<a href="/german/irregular-verbs">{`Unregelmäßige Verben (${VerbenData.length})`}</a>
					<a href="/german/goethe">{`Goethe (${Goethe.length})`}</a>
				</ul>
			</details>
		</article>

	  <span class="hidden md:flex  bottom-2 right-4 text-3xl">
      Dark
    </span>

    <div class="text-4xl md:hidden ml-auto">
      Menu
    </div>
  </div>
	

	<NavbarMobile />
</nav>
