<script>
    import "../app.scss";
    import Hero from "./hero/hero.svelte"
    import About from "./about/about.svelte"
    import Project from "./project/project.svelte"
</script>


<div class="scroll-snap">
    <section>  
        <div class="wrap">
            <Hero />
        </div>
    </section>
    <section>  
        <div class="wrap">
            <Project />
        </div>
    </section>
    
    
    <section class="mt-32">
        <div class="wrap" >
            <About  />
        </div>
    </section>
</div>




<style lang="scss">

.wrap{
    padding-left: 24px;
    padding-right: 24px;
    margin-right: auto;
    margin-left: auto;
    max-width: 1136px;

    padding-top: 24px;
    padding-bottom: 32px;
    
}
@media (max-width: 768px) {
    .wrap{
        padding-left: 12px;
        padding-right: 12px;
    }
}
// .scroll-snap {
//   width: 100vw;
//   height: 100vh;
//   scroll-snap-type: y mandatory;
//   scroll-snap-type: mandatory;
//   overflow: auto;
// }

section {
  scroll-snap-align: start;
}
</style>    