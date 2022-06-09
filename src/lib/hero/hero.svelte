<script>
    import {hero} from "$lib/data.json"
    import LogoSvgXL from "$lib/assets/loli-svg.svelte"
</script>

<div class="hero flex relative justify-around font">
    <div></div>
    <div class="max-w-xs mt-20">
        <LogoSvgXL />
    </div>
    <div class="flex justify-center flex-col mx-5 mb-16 md:mb-5 mt-0 md:mt-10">
        <h1 class="text-5xl mb-8 md:mb-3 tracking-wide">{@html hero.h1}</h1>
        <p class="text-1xl tracking-wide max-w-lg">{@html hero.p}</p>
    </div>
    <div></div>
</div>

<style>
@media (max-width: 768px) {
    .hero{
    height: calc(100vh - 60px);
}
}

.font{
    font-family: 'Montserrat', sans-serif;
}
p{
    padding-left: 4px;
}
</style>
