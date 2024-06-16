<script>
  let message = "";
  import Sidebar from "./Sidebar.svelte";
  import Heading from "./Heading.svelte";
  import Search from "./Search.svelte";
</script>

<svelte:head>
  <title>Main</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="container">
  <Sidebar />
  <Heading />
  <Search />
</div>

<style>
  .container {
    display: flex;
    height: 98vh;
    background-color: white;
  }
</style>
