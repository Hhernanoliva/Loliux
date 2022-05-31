<script>
    import img from "$lib/img/loli.webp"
    import EllipseGradient from "$lib/assets/ellipse-gradient.svelte";

    
    export let sobreMi;
</script>

<div class="flex flex-col md:flex-row w-full justify-center my-10">
        <div class="relative mx-10 img-content relative">
            <img src="{img}" alt="">
            <div class="absolute inset-0 spin">
                <EllipseGradient />
            </div>

        </div>
    <div class="p">
        {@html sobreMi}
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