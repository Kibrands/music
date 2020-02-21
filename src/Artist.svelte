<script>
  export let artist = {};
</script>

<div class="card">
  <img src={artist.image} class="rounded float-left" alt={artist.nick} />
  <h4 class="title">{artist.nick}</h4>
  <p>Nombre: {artist.name}</p>
  <p>Apellidos: {artist.lastName}</p>
  <slot />
</div>
