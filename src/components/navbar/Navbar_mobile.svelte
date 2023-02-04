<script>
	const styles = {
		nav: 'flex justify-center items-center w-full  min-h-[100px] shadow-xl z-[400] px-4',
		nav__div: 'navDetails w-full h-full flex items-start  relative text-xl ',
		aside: 'logo sm:w-1/3 ',
		article: 'justify-around items-start w-full h-full hidden md:flex',
		nav__ul: 'flex flex-col border-solid border-t-4 border-sky-400 navDetails'
	};

	const IrregularVerbs = [0];
	const VerbenData = [0];
	const OxfordB1 = [0];
	const OxfordB2 = [0];
	const OxfordC1 = [0];

	const LukesPhrasal = [0];
	const Goethe = [0];

	const nav = false;
</script>

<div class={nav ? 'snap-x z-10  fixed left-0 top-0 w-full h-screen bg-black/70' : 'z-0'}>
	<div
		class={nav
			? 'responsiveMenu fixed left-0 top-0 w-[85%] sm:w-[60%] md:w-[45%] h-screen mobile__Nav p-4 sm:p-8 ease-in duration-500'
			: 'fixed top-10 left-[-100%] ease-in duration-500'}
	>
		<div class="flex justify-between items-center">
			<aside class="logo sm:mr-40">
				<a href="/">
					Learn <strong>languages</strong>
				</a>
			</aside>
			<div class="navClose rounded-full shadow-lg shadow-gray-400 p-3 cursor-pointer">
				CloseIcon
			</div>
		</div>
		<div class="mottoCover border-b border-gray-300 my-4 text-sm sm:text-lg">
			<p>Evolution means everyday learning</p>
		</div>
		<nav>
			<ul class="flex flex-col  z-20">
				<div class="flex justify-between items-center">
					<a class="py-4 uppercase" href="/"> Home </a>
					<span class="bottom-2 right-4 text-3xl"> DarkomodeIcon </span>
				</div>

				<main>
					<details class="py-4 cursor-pointer">
						<summary class="uppercase border-gray-300 border-b logo">
							<strong>English</strong>
						</summary>
						<ul class="flex flex-col navDetails">
							<a href="/english/irregular-verbs">{`Irregular verbs (${IrregularVerbs.length})`}</a>
							<a href="/english/search-irregular">{`Irregular list (${IrregularVerbs.length})`}</a>
							<a href="/english/oxford-B1">{`Oxford B1 (${OxfordB1.length})`}</a>
							<a href="/english/oxford-B2">{`Oxford B2 (${OxfordB2.length})`}</a>
							<a href="/english/oxford-C1">{`Oxford C1 (${OxfordC1.length})`}</a>
							<a href="/english/phrasal-verbs">{`Lukes Phrasal (${LukesPhrasal.length})`}</a>
							<a href="/english/pagination">Pagination</a>
						</ul>
					</details>

					<details class="cursor-pointer">
						<summary class="uppercase border-gray-300 border-b logo">
							<strong> Deutsch</strong>
						</summary>
						<ul class="flex flex-col navDetails">
							<a href="/german/german">{`Unregelmäßige Verben (${VerbenData.length})`}</a>
							<a href="/german/goethe">{`Goethe (${Goethe.length})`}</a>
						</ul>
					</details>
				</main>
			</ul>
		</nav>
	</div>
</div>

<style>

</style>
