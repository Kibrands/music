<script>
  import { onMount, getContext } from "svelte";
  import { jsonData } from "./store.js";
  import Search from "./Search.svelte";
  import Artist from "./Artist.svelte";
  import { Link } from "svelte-routing";

  const URL = getContext("URL");
  let search = "";
  let artist = {};

  onMount(async () => {
    const response = await fetch(URL.artists);
    const data = await response.json();
    $jsonData = data;
  });

  $: regex = new RegExp(search, "i");
  $: data = search
    ? $jsonData.filter(item => regex.test(item.nick))
    : $jsonData;
</script>

<h1>ARTISTAS</h1>
<Search bind:search />

<div class="container">
  {#each data as artist}
    <Artist {artist}>
      <div style="text-align: right">
        <Link to="/songs?id={artist._id}">Ver canciones</Link>
      </div>
    </Artist>
  {/each}
</div>
