<script>
  import { Route } from "svelte-routing";
  import Index from "./Index.svelte";
  import Artists from "./Artists.svelte";
  import Footer from "./Footer.svelte";
  import Songs from "./Songs.svelte";
</script>

<main id="main" class="pt-4">
  <Route path="/" component={Index} />
  <Route path="/artists" component={Artists} />
  <Route path="/songs" component={Songs} />
  <Footer />
</main>
