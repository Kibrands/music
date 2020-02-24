<script>
  export let search;
</script>

<style>
  .text-align-right {
    text-align: right !important;
    font-size: 1.2em;
  }
</style>

<div class="form-group row" id="searchDiv">
  <label
    id="search-label"
    for="search"
    class="col-sm-2 col-form-label text-align-right">
    Buscar
  </label>
  <div class="col-sm-10">
    <input bind:value={search} type="search" class="form-control" id="search" />
  </div>
</div>
