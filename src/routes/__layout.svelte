<script>
  import "../app.scss";
  import Navbar from "$lib/navbar/index.svelte"
  import Sidebar from "$lib/navbar/sidebar.svelte"
  // DATA DEL NAVBAR
  import {navbar}  from "$lib/data.json"
  const dbNavlink = navbar.links
  
  let open = false
</script>

<Sidebar bind:open dbNav={dbNavlink} />
<Navbar bind:sidebar={open}/>

<slot />
