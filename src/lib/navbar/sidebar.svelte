<script>
    export let dbNav;
    export let open = false;
    
</script>


<aside class="absolute w-full h-full shadow-lg md:hidden" class:open>
    <div id="links" class="mr-2 h-full flex flex-col items-center justify-center">
         {#each dbNav as link }
            <a href="{link.path}" class="leading-none text-3xl px-5 pt-3 pb-4 my-10 mx-2 text-base tracking-wide transition ease-in-out delay-100 hover:-translate-y-1 hover:font-medium  hover:bg-slate-600 duration-300 rounded-lg ...">{link.name}</a>
        {/each} 
    </div>
</aside>

<style>
	aside {
        z-index: 10;
		top: -100%;
		transition: top 0.3s ease-in-out;
        background-color: var(--primary-color);
	}
	
	.open {
		top: 0
	}
</style>