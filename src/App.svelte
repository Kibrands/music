<script>
  import { setContext } from "svelte";
  import { Router } from "svelte-routing";
  import { writable } from "svelte/store";
  import Content from "./Content.svelte";
  import Nav from "./Nav.svelte";

  const URL = {
    artists: "https://kibrandsbackend.herokuapp.com/api/artists/",
    songs: "https://kibrandsbackend.herokuapp.com/api/songs/"
  };
  setContext("URL", URL);
</script>

<style>
  :global(body) {
    background-color: gainsboro !important;
  }

  :global(ul li a) {
    color: white !important;
  }

  :global(ul li a:hover) {
    text-decoration: none !important;
    color: lightgray !important;
  }
</style>

<Router>
  <Nav />
  <Content />
</Router>
