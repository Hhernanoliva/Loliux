<script>
    import {hero} from "$lib/data.json"
    import LogoSvgXL from "$lib/assets/loli-svg.svelte"
</script>

<div class="hero flex relative justify-center font">
    <div class="max-w-xs">
        <LogoSvgXL />
    </div>
    <div class="flex justify-center flex-col mx-5">
        <h1 class="text-4xl xl:text-5xl mb-3 tracking-wide">{@html hero.h1}</h1>
        <p class="text-1x1 xl:text-2x1 tracking-wide max-w-lg">{@html hero.p}</p>
    </div>
</div>

<style>
@media (max-width: 768px) {
    .hero{
    height: calc(100vh - 60px);
}
}
.hero{
    height: calc(100vh - 71px);
}
.font{
        font-family: 'Montserrat', sans-serif;
    }
</style>
