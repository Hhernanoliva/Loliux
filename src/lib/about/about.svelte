<script>
    import img from "$lib/img/loli.png"
</script>

<div class="flex flex-col md:flex-row w-full justify-center my-10">
    <!-- <div class="img-about"> -->
        <div class="relative mx-10 img-content img-about ">
            <img src="{img}" alt="">
        </div>
    <!-- </div> -->


    <div class="p">
        text 
    </div>
</div>

<style>
    .img-about{
        position: relative;
        width: 260px;
        height: 260px;
    }

    .img-content{
        max-width: 260px;
        max-height: 260px;
    }
    img{
        width: 100%;
        display: block;
        border-radius: 50%;
        z-index: 1;
    }

    .img-about::before{
        content: "";
        position: absolute;
        inset: -6px;
        border: 3px solid #008BEF;
        border-color: radial-gradient(#A181FF,#64F083,#FFAA5C,#FF97C9);
        border-top-color: #A181FF;
        border-bottom-color: #64F083;
        border-left-color: #FFAA5C;
        border-right-color: #FF97C9;
        border-radius: 50%;
        z-index: 2;
        animation: spin 0.6s linear infinite;
        filter: blur(2px);
    }

    @keyframes spin{
        to { transform: rotate(360deg);}
    }
</style>