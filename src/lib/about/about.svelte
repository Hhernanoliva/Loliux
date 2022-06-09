<script>
    import img from "$lib/img/loli.webp"
    import EllipseGradient from "$lib/assets/ellipse-gradient.svelte";
    import {about} from "$lib/data.json"

</script>

<div class=" md:my-20 w-full grid grid-cols-1 md:grid-cols-4 gap-x-5">

    <div class="relative md:mx-10 img-content ">
        <img src="{img}" alt="" >
        <div class="absolute inset-0 spin ">
            <EllipseGradient />
        </div>
    </div>


    <div class="p col-span-3" >
        <h3 class="">
            {@html about.h3}
        </h3>
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

    .spin{
        animation: spin 10s linear infinite;
    }
    @keyframes spin{
        to { transform: rotate(360deg);}
    }
</style>