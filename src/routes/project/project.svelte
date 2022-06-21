<script>
    import projectDB from "$lib/projectDB"
 
    // IMAGENES
    import logoTutoragio from "$lib/imgs/tutoragio.png"
    import logo2 from "$lib/imgs/enlanube.png"
    //  /IMAGENES
    
    let logo1 = logoTutoragio
</script>

<div id="main" class="flex flex-wrap flex-row justify-center justify-items-center w-full">

    {#each projectDB as { title, copy, time, src, imgWidth, imgHeight } }
        <div class="shadow-md drop-shadow-md rounded-2xl max-w-xs p-2 mb-10 md:mb-20 mx-0 md:mx-12 bg-white">
            <article>
                <a href="">
                <div class="h-64 md:h-72 overflow-hidden flex justify-center justify-items-center">
                    <img {src} alt="adidas" style="width: {imgWidth}px; height: {imgHeight}px" class="p-5 m-auto " />
                </div>
                <div class="m-1 p-4 rounded-lg bg-secondary">
                    <h4 class="txt-primary font-bold title">
                        {title}
                    </h4>
                    <p class="txt-primary copy">
                        {copy}
                    </p>
                    <div class="flex items-center justify-between time mt-1">
                        <p class="txt-primary">
                            {time}
                        </p>
                        <button type="button" class="w-10 h-10 text-base font-medium rounded-full text-white bg-blue btn mt-1" style="">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" class="mx-auto" fill="white" viewBox="0 0 1792 1792">
                                <path d="M1600 736v192q0 40-28 68t-68 28h-416v416q0 40-28 68t-68 28h-192q-40 0-68-28t-28-68v-416h-416q-40 0-68-28t-28-68v-192q0-40 28-68t68-28h416v-416q0-40 28-68t68-28h192q40 0 68 28t28 68v416h416q40 0 68 28t28 68z">
                                </path>
                            </svg>
                        </button>
                    </div>
                </div>
                </a>
            </article>
        </div>
	{/each}

</div>

<style>
    .title{

    }
    .copy{

    }
    .time{

    }
    .img{

    }
    .btn{

    }
</style>