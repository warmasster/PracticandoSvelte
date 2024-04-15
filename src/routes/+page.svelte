<script>
    import "../app.css";
    let num = 0;
    let nums = [];
    let rand = 0;
    function increment(){
        num++;
    }

    function decrement(){
        num = ((num > 0) ? (num = num-1) : (num = 0))
    }

    function gen_nums(){
        console.log(nums);
        nums = [];
        for(let i = 0; i < num; i++){
            rand = Math.random()*100;
            nums.push(Math.floor(rand));
        }
    }
</script>

<div class="flex justify-center darker-bg nav">
    <h1 class="title light">Numero aleatorio</h1>
</div>

<div class="flex flex-col flex-wrap justify-center pt-6 px-100 standalone-center">
    <div class="flex">
        <button class="mx-10 darker-bg btn hover:cursor-pointer" on:click={decrement}>
            <span class="minus-simbol"></span>
        </button>
        
        <div class="w-24 text-center ">
            <h2 class="text-5xl font-bold sm:text-6xl light">{num}</h2>
        </div>
        
        <button class="mx-10 darker-bg btn hover:cursor-pointer" on:click={increment}>
            <span class="plus-simbol-1"></span>
            <span class="plus-simbol-2"></span>
        </button>
    </div>

    <div class="pt-7">
        <button class="flex flex-wrap justify-center m-0 mx-10 darker-bg btn-l hover:cursor-pointer" on:click={gen_nums}>
            <h2 class="text-2xl font-bold sm:text-4xl light">Generar numeros</h2>
        </button>
    </div>
</div>

{#if nums.length > 0}
    {#each nums as rand_num, i}
        <div><h1>{rand_num}</h1></div>
    {/each}
{/if}

<style lang="postcss">
    
    .darker-bg{background-color: rgb(0, 60, 67)}
    .mid-bg{background-color: rgb(19, 93, 102)}
    .light-bg{background-color: rgb(119, 176, 170)}
    .lighter-bg{background-color: rgb(227, 254, 247)}
    
    .darker{color: rgb(0, 60, 67)}
    .mid{color: rgb(19, 93, 102)}
    .light{color: rgb(119, 176, 170)}
    .lighter{color: rgb(227, 254, 247)}
    
    .standalone-center {
        display: table;
        margin-right: auto;
        margin-left: auto;
    }
    .minus-simbol{
         background-color: rgb(119, 176, 170);
         border-radius: 2px;
         height: 3rem;
         width: 0.5rem;
         rotate: 90deg;
    }
    
    .plus-simbol-2{
        position: absolute;
         background-color: rgb(119, 176, 170);
         border-radius: 2px;
         height: 3rem;
         width: 0.5rem;
         rotate: 90deg;
    }
    .plus-simbol-1{
        position: absolute;
         background-color: rgb(119, 176, 170);
         border-radius: 2px;
         height: 3rem;
         width: 0.5rem;
    }
    
    .btn {
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 10px;
        height: 5rem;
        width: 5rem;
        padding: 5px;
    }

    .btn-l {
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 10px;
        height: 4rem;
        width: 21rem;
        padding: 5px;
    }
    .title {
         font-size: 40px;
         font-weight: bolder;
    }
    
    .nav {border-radius:0px 0px 10px 10px;}

    :global(html) {
        background-color: rgb(19, 93, 102);
    }
</style>