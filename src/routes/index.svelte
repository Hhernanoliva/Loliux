<script>
    import "../app.scss";
    import Hero from "$lib/hero/hero.svelte"
    import About from "$lib/about/about.svelte"
</script>



<header>
    <div class="wrap">
        <Hero />
    </div>

</header>

<section>
    <div class="wrap">
    <About />
    </div>
</section>



<style lang="scss">

.wrap{
    padding-left: 24px;
    padding-right: 24px;
    margin-right: auto;
    margin-left: auto;
    max-width: 1136px;

    padding-top: 24px;
    padding-bottom: 32px;
    background-color: rgb(77, 55, 151);
    
}

</style>    