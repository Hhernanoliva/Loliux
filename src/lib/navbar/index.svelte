<script>
    import Burger from "$lib/navbar/hamburger.svelte"
    import LogoSvg from "$lib/assets/logo-svg.svelte"
    import {navbar}  from "$lib/data.json"

    export let sidebar = false;

</script>



<nav>
    <div id="navbar" class="flex justify-between items-center px-2 py-1 md:py-3 max-h-20 ">

        <a id="logo" href="/" class="flex items-center">
            <div class="md:hidden px-2">
                <LogoSvg />
            </div>
            
            <p class="text-2xl md:text-3xl tracking-normal tracking-widest pt-1 md:pt-0 pl-2" style="font-family: 'Forum', cursive;">{navbar.logoName}</p>
        </a>

        <div id="links" class="mr-2 hidden md:flex">
            {#each navbar.links as link }
                <a href="{link.path}" class="px-2 mx-2 text-base tracking-wide transition ease-in-out delay-100 hover:-translate-y-1 hover:scale-y-90  hover:bg-amber-200 duration-500 rounded-lg ...">{link.name}</a>
            {/each}
        </div>

        <div class="flex md:hidden">
            <Burger bind:open={sidebar} />
        </div>
    </div>
</nav>

<style lang="scss">
    
    // nav{
    //     z-index: 100;
    // }
    #navbar{
        background-color: var(--primary-color);
        
    }
    #links{
        font-family: 'Montserrat', sans-serif;
    }


</style>