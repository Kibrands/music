<script>
  import { Link } from "svelte-routing";
</script>

<nav class="navbar navbar-expand-lg navbar-dark bg-dark border border-dark pl-4">
  <div class="mr-4">
    <Link to="/">
      <img class="float-left rounded" src="img/logo.png" width="170" alt="KBS Music" />
    </Link>
  </div>
  <button
    class="navbar-toggler"
    type="button"
    data-toggle="collapse"
    data-target="#navbarToggler"
    aria-controls="navbarToggler"
    aria-expanded="false"
    aria-label="Menú">
    <span class="navbar-toggler-icon" />
  </button>
  <div class="collapse navbar-collapse" id="navbarToggler">
    <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
      <li class="nav-item mr-2">
        <Link to="/artists">Artistas</Link>
      </li>
      <li class="nav-item">
        <Link to="/songs">Canciones</Link>
      </li>
    </ul>
  </div>
</nav>
