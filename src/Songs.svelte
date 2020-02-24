<script>
  import { onMount, getContext } from "svelte";
  import { jsonData } from "./store.js";
  import Search from "./Search.svelte";
  import Song from "./Song.svelte";

  const URL = getContext("URL");
  let search = "";
  let song = {};
  let artistId = findGetParameter("artistId");
  let fetchURL = URL.songs;

  onMount(async () => {
    if (artistId != null && artistId != undefined && artistId != "") {
      fetchURL += "artist/" + artistId;
    }
    const response = await fetch(fetchURL);
    const data = await response.json();
    $jsonData = data;
  });

  $: regex = new RegExp(search, "i");
  $: data = search
    ? $jsonData.filter(item => regex.test(item.title))
    : $jsonData;

  function findGetParameter(parameterName) {
    var result = null,
      tmp = [];
    location.search
      .substr(1)
      .split("&")
      .forEach(function(item) {
        tmp = item.split("=");
        if (tmp[0] === parameterName) result = decodeURIComponent(tmp[1]);
      });
    return result;
  }
</script>

<div class="container">
  <h1>CANCIONES</h1>
  <Search bind:search />
  <div class="row">
    {#each data as song}
      <div class="col-xs-12 col-md-4">
        <Song {song}>
          <div style="text-align: right" />
        </Song>
      </div>
    {/each}
  </div>
</div>
