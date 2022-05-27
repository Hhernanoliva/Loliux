<script>
    import {hero} from "$lib/data.json"
    import LogoSvgXL from "$lib/assets/loli-svg.svelte"
</script>

<div class="flex relative justify-center mt-20 font">
    <div class="max-w-xs">
        <LogoSvgXL />
    </div>
    <div class="flex justify-center flex-col">
        <h1>{@html hero.h1}</h1>
        <h2>{@html hero.h2}</h2>
        <p>{@html hero.p}</p>
    </div>
</div>

<style>
    .font{
        font-family: 'Montserrat', sans-serif;
    }
</style>
