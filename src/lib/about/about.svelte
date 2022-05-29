<script>
    import img from "$lib/img/img-about.webp"
</script>

<div class="flex flex-col md:flex-row w-full justify-center my-10">
    <div class="relative mx-10 img-about">
        <img src="{img}" alt="">
    </div>
    <div class="p">
        text 
    </div>
</div>

<style>
    .img-about{
        max-width: 150px;
        position: relative;
    }

    img{
        width: 100%;
        display: block;
        border-radius: 50%;
    }

    .img-about::before{
        content: "";
        position: absolute;
        inset: -15px;
        border: 6px solid rgb(255, 128, 128);
        border-top-color: #fff;
        border-bottom-color: #ababab;
        border-radius: 50%;
        z-index: -1;
        animation: spin 3s linear infinite;
    }

    @keyframes spin{
        to { transform: rotate(360deg);}
    }
</style>