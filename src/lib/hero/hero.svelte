<script>
    import {hero} from "$lib/data.json"
    import LogoSvgXL from "$lib/assets/loli-svg.svelte"
    import LogoSvg from "$lib/assets/logo-svg.svelte"
</script>

<main class="hero flex relative font justify-center md:justify-start">
        <div></div>
        <div class="max-w-xs mt-20">
            <LogoSvgXL />
        </div>
        <div class="flex justify-center flex-col mx-5 mb-16 md:mb-5 mt-0 md:mt-10 md:pl-10">
            <div class="md:hidden px-2 w-full flex justify-center pb-16 pr-14">
                <LogoSvg />
            </div>
            <h1 class="mb-8 md:mb-3 tracking-wide leading-tight">{@html hero.h1}</h1>
            <p class="tracking-wide max-w-lg">{@html hero.p}</p>
        </div>
        <div></div>
</main>

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
