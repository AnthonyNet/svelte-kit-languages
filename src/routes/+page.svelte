<script>
    import Navbar from '../components/navbar/Navbar.svelte';
    const styles = {
  section:
    "responsiveSection flex flex-col justify-center items-center w-full min-h-[88vh] h-auto sm:h-[90%] border-red-300  border-t-2",
  card__div:
    "mainCard w-[300px] h-[420px] cursor-pointer group perspective",
  card__div__div:
    "preserve-3d group-hover:my-rotate-y-180  w-full h-full duration-1000",
  card__div__div__div: "w-full h-full",
  cardBack:
    "mainCardBack bg-white my-rotate-y-180  backface-hidden w-full h-full mt-[-420px] overflow-hidden shadow-lg shadow-gray-400",
  cardBack__div:
    "text-center flex flex-col items-center h-full text-gray-800 px-2 pb-24 ",
  cardBack__div__btn:
    "bg-teal-500 px-6 py-2 mt-[8rem] mb-8 font-semibold text-white rounded-full delay-500 duration-1000 scale-0 group-hover:scale-125",
  button:
    "bg-teal-500 px-6 py-2 mt-[8rem] mb-8 font-semibold text-white rounded-full delay-500 duration-1000 scale-0 group-hover:scale-125",
};
</script>


<Navbar />

<section class={styles.section}>

    <h1 class="my-2 sm:mt-0">
  Welcome
    </h1>
   

    <div class={styles.card__div}>
      <div class={styles.card__div__div}>
        <div class={styles.card__div__div__div}>
         <img  src="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fimg4.wikia.nocookie.net%2F__cb20081229142345%2Ffallout%2Fimages%2F2%2F2a%2FFallout2front.jpg&f=1&nofb=1"  class="w-full h-full border-2"
         alt="fallout-logo">
        </div>
        <div class={styles.cardBack}>
          <div class={styles.cardBack__div}>
            <h2 class="my-4 text-3xl font-semibold self-center">
        Nadpis
            </h2>

         
            <button class={styles.button}>Last update:</button>
            <h2 class="text-sm font-semibold ">
          hhh
            </h2>
          </div>
        </div>
      </div>
    </div>

 
  </section>

<style>

.my-rotate-y-180 {
  transform: rotateY(180deg);
}

.preserve-3d {
  transform-style: preserve-3d;
}

.perspective {
  perspective: 1000px;
}

.group:hover .group-hover\:my-rotate-y-180 {
  transform: rotateY(180deg);
}
.backface-hidden {
  backface-visibility: hidden;
}

</style>
