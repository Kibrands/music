<script>
  export let artist = {};
</script>

<style>
  .artist-card {
    background-color: white;
    color: black;
  }
</style>

<div class="rounded card p-3 my-2 artist-card">
  <div class="row">
    <div class="col-md-2 col-xs-12">
      <img
        src={artist.image}
        class="rounded-circle img-fluid"
        alt={artist.nick} />
    </div>
    <div class="col-md-10 col-xs-12">
      <div class="ml-2">
        <h5 class="title">{artist.nick}</h5>
        <p>Nombre: {artist.name}</p>
        <p>Apellidos: {artist.lastName}</p>
      </div>
    </div>
  </div>
  <slot />
</div>
