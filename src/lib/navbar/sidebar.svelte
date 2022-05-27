<script>

    export let links = [];
	export let open = false;
</script>

<aside class="absolute w-full h-full shadow-lg" class:open>
    <!-- <div id="links" class="mr-2 hidden md:flex">
        {#each links as link }
            <a href="{link.path}" class="px-2 mx-2 text-base tracking-wide transition ease-in-out delay-100 hover:-translate-y-1 hover:scale-y-90  hover:bg-amber-200 duration-500 rounded-lg ...">{link.name}</a>
        {/each}
    </div> -->
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