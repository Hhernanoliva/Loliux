<script>
    import Burger from "$lib/navbar/hamburger.svelte"

    import {navbar}  from "$lib/data.json"

    export let sidebar = false;

</script>

<div id="navbar" class="flex justify-between items-center px-2 py-1 md:py-3 max-h-20 ">

    <a id="logo" href="/" class="flex items-center">
        <p class="text-2xl md:text-3xl tracking-normal tracking-widest pt-1 md:pt-0 pl-2 md:pl-6" style="font-family: 'Forum', cursive;">{navbar.logoName}</p>
    </a>

    <div id="links" class="mr-2 hidden md:flex">
        {#each navbar.links as link }
            <a href="{link.path}" class="px-2 mx-2 text-base tracking-wide">{link.name}</a>
        {/each}
    </div>

    <div class="flex md:hidden justify-end">
        <Burger bind:open={sidebar} />
    </div>
</div>

<style lang="scss">
    
    #navbar{
        background-color: var(--primary-color);
        
    }
    #links{
        font-family: 'Montserrat', sans-serif;
    }


</style>