<script>
    import {hero} from "$lib/data.json"
    import LogoSvgXL from "$lib/assets/loli-svg.svelte"
    import LogoSvg from "$lib/assets/logo-svg.svelte"
</script>

<main class="hero flex justify-center items-center relative font">
        <div class="max-w-xs ">
            <LogoSvgXL />
        </div>
        <div class="flex md:justify-center flex-col mb-0 md:mb-5 md:pl-10">
            <div class="md:hidden px-2 w-full flex justify-center pb-5 pr-8 md:pb-16">
                <LogoSvg />
            </div>
            <h1 class="mb-3 md:mb-3 tracking-wide leading-tight">{@html hero.h1}</h1>
            <p class="tracking-wide max-w-lg">{@html hero.p}</p>
        </div>
</main>

<style>
@media (min-width: 768px) {

}
.hero{
    height: calc(100vh - 60px);}
.font{
    font-family: 'Montserrat', sans-serif;
}

p{
    padding-left: 4px;
}
</style>
