<script>
    import "../app.css";
    export let randnum = 0;
    export let index = 0;
</script>

{#if index % 2 == 0}
    <div class="flex num-row darker-bg light">
        <div  class="inner-comp">
            <h1 class="text-center mx-7 w-7">{randnum}</h1>
        </div>

        <div  class="inner-comp">
            <a class="underline mx-7" href="https://es.wikipedia.org/wiki/{randnum}">Info</a>
        </div>

        <div  class="inner-comp">
            <p class="w-12 text-left mx-7">Par</p>
        </div>
    </div>

{:else}
    <div class="flex num-row light-bg darker">
        <div  class="inner-comp">
            <h1 class="text-center mx-7 w-7">{randnum}</h1>
        </div>

        <div  class="inner-comp">
            <a class="underline mx-7" href="https://es.wikipedia.org/wiki/{randnum}">Info</a>
        </div>

        <div  class="inner-comp">
            <p class="w-12 text-left mx-7">Impar</p>
        </div>
    </div>
{/if}

<style>
    .num-row {
        font-size: large;
        border-radius: 0.5rem;
        font-weight: bolder;
        padding: 0.5rem;
        margin-top: 2%;
        margin-left: 10%;
        margin-right: 10%;
    }
    .inner-comp {
        border-right: 1px solid rgb(227, 254, 247);
        width: 44px;
        width: fit-content;
    }
</style>