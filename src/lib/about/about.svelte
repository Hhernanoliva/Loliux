<script>
    import img from "$lib/assets/img/loli.webp"
    import EllipseGradient from "$lib/assets/ellipse-gradient.svelte";
    import {about} from "$lib/data.json"
    import LogoBehance from "$lib/assets/logo-behance.svelte"

</script>


<div class="md:my-10 w-full grid grid-cols-1 md:grid-cols-3 gap-x-5" >
    <div class=" m-auto relative img-content justify-center">
            <img src="{img}" alt="Foto de Leonela justify-center" >
            <div class="absolute inset-0 spin justify-center">
                <EllipseGradient />
            </div>
    </div>
    <div class="p col-span-2" >
        <h2 >
            {@html about.h3}
        </h2>
        <p class="w-full">
            {@html about.p}
        </p>
    </div>
</div>

<div class="md:my-10 w-full grid grid-cols-1 md:grid-cols-3 gap-x-5" >
    <div>
    </div>
    <div class="p col-span-2" >
        <div class="flex flex-col">
            <p class="span">
                <i>{@html about.span}</i>
            </p>
            <div class="flex">
                <LogoBehance />
            </div>

        </div>

    </div>

</div>

<div class="md:my-10 w-full grid grid-cols-1 md:grid-cols-3 gap-x-5" >
    <div>
    </div>
    <div class="p col-span-2" >
        <p class="span" >
            <i>{@html about.spann}</i>
        </p>
    </div>
</div>

<style>
    .img-content{
        width: 200px;
        height: 200px;
    }
    img{
        width: 100%;
        display: block;
        border-radius: 50%;
        z-index: 1;
    }
    .span{
        font-size: 0.875rem;
    }
    .spin{
        animation: spin 10s linear infinite;
    }
    @keyframes spin{
        to { transform: rotate(360deg);}
    }
</style>