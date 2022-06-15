<script>
  import "../app.scss";
  import Navbar from "$lib/navbar/navbar.svelte"
  import Sidebar from "$lib/navbar/sidebar.svelte"
  
  // DATA DEL NAVBAR
  import {navbar}  from "$lib/data.json"
  const dbNavlink = navbar.links
  
  let open = false
</script>


<section>
  <Sidebar bind:open dbNav={dbNavlink} />
  <nav class="nav">
    <Navbar bind:sidebar={open}/>
  </nav>
</section>

<slot />


<style>
  .nav{
    position: fixed;
    top: 0;
    width: 100%;
    height: 60px;
    z-index: 10;
  
  }
</style>
