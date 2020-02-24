<script>
  export let song = {};
  let releaseDate = new Date(song.releaseDate);
</script>

<style>
  .song-card {
    background-color: white;
    color: black;
  }
</style>

<div class="card rounded p-3 my-2 song-card">
  <img
    src={song.cover}
    class="rounded img-fluid"
    alt={song.title} />
  <h5 class="title">{song.title}</h5>
  <p>Precio: {song.price}</p>
  <p>Fecha de publicación: {releaseDate.getYear()}</p>
  <p>Discográfica: {song.label}</p>
  <slot />
</div>
