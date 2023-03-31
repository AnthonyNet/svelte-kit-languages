<script context="module">

</script>

<script lang="ts">
    let score:number = 0;
    export let word:string = '';
    export let props:any;
 /*   console.log(props)
    console.log('----') */


    </script>

   <li class="flex flex-col items-center">
        <input type="text" class="border-2 py-1 m-2 text-center w-full" bind:value={word}/>
    </li>
