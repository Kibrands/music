<script>
  import { Route } from "svelte-routing";
  import Index from "./Index.svelte";
  import Artists from "./Artists.svelte";
  import Footer from "./Footer.svelte";
</script>

<main id="main">
  <Route path="/" component={Index} />
  <Route path="/artists" component={Artists} />
  <Footer />
</main>
