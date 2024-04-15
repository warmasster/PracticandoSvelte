<script>
    import "../app.css";
    let num = 0;

    function increment(){
        num++;
    }

    function decrement(){
        num = ((num > 0) ? (num = num-1) : (num = 0))
    }
</script>

<div class="flex justify-center darker-bg nav">
    <h1 class="title light">Numero aleatorio</h1>
</div>

<div class="flex justify-center pt-6">
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


<style lang="postcss">
    
    .darker-bg{background-color: rgb(0, 60, 67)}
    .mid-bg{background-color: rgb(19, 93, 102)}
    .light-bg{background-color: rgb(119, 176, 170)}
    .lighter-bg{background-color: rgb(227, 254, 247)}
    
    .darker{color: rgb(0, 60, 67)}
    .mid{color: rgb(19, 93, 102)}
    .light{color: rgb(119, 176, 170)}
    .lighter{color: rgb(227, 254, 247)}
    
    .minus-simbol{
         background-color: rgb(119, 176, 170);
         border-radius: 0.5vh;
         height: 9vh;
         width: 1.5vh;
         rotate: 90deg;
    }
    
    .plus-simbol-2{
        position: absolute;
         background-color: rgb(119, 176, 170);
         border-radius: 0.5vh;
         height: 9vh;
         width: 1.5vh;
         rotate: 90deg;
    }
    .plus-simbol-1{
        position: absolute;
         background-color: rgb(119, 176, 170);
         border-radius: 0.5vh;
         height: 9vh;
         width: 1.5vh;
    }
    
    .btn {
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 10px;
        height: 12vh;
        width: 12vh;
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