<script>
  export let search;
</script>

<label>
  <div class="form-group">
    <label for="search">Buscar</label>
    <input bind:value={search} class="form-control" type="search" id="search" />
  </div>
</label>
