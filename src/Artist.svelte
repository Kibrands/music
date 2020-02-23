<script>
  export let artist = {};
</script>

<style>
  .artist-card {
    background-color: white;
    color: black;
  }
</style>

<div class="rounded container-fluid p-3 my-2 artist-card">
  <img
    src={artist.image}
    width="150"
    class="rounded-circle float-left img-fluid"
    alt={artist.nick} />
  <div class="ml-2">
    <h5 class="title">{artist.nick}</h5>
    <p>Nombre: {artist.name}</p>
    <p>Apellidos: {artist.lastName}</p>
  </div>
  <slot />
</div>
