<script>
  import "../app.scss";
  import Navbar from "$lib/navbar/index.svelte"
  import Sidebar from "$lib/navbar/sidebar.svelte"
  let open = false
</script>

<Sidebar bind:open/>
<Navbar bind:sidebar={open}/>

<slot />
