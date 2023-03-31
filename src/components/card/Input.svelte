<script context="module">
const style = {
	li: "flex flex-col items-center",
	li_right: "bg-green-500",
	input: "border-2 py-1 m-2 text-center w-full"
}
</script>

<script lang="ts">
    let score:number = 0;
    export let word:string = '';
    export let props:any;
	export let definition:string = '';

    </script>
// check value in input
   <li class={word===props?style.li + " " + style.li_right:null}>
        <input type="text" class={style.input} placeholder={definition} bind:value={word}/>
    </li>
