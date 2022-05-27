<script>
  import "../app.scss";
  import Navbar from "$lib/navbar/navbar.svelte"
  import Sidebar from "$lib/navbar/sidebar.svelte"
  
  // DATA DEL NAVBAR
  import {navbar}  from "$lib/data.json"
  const dbNavlink = navbar.links
  
  let open = false
</script>


<header>
  <Sidebar bind:open dbNav={dbNavlink} />
  <nav class="w-screen">
    <Navbar bind:sidebar={open}/>
  </nav>

</header>

<slot />
