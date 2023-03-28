<script context="module">

</script>

<script lang="ts">
    //define props

    let score:number = 0;
    export let word:string = '';
    export let props:any;
 /*   console.log(props)
    console.log('----') */


    </script>

    {#if word===props}
    {score +=1}
    <li class="hidden">
        <span>{word}</span>
        <input type="text" class="border-2 py-1 m-2 text-center" bind:value={word}/>
    </li>
    {/if}
    {#if word!==props}
    <li class="flex flex-col items-center   absolute">
        <span class="h-[40px] bg-white w-[90%]">{word}</span>
        <input type="text" class="border-2 py-1 m-2 text-center w-full" bind:value={word}/>
    </li>
    {/if}
