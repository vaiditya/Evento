<script>
  import HomePage from "./pages/HomePage.svelte";
  import EventPage from "./pages/EventPage.svelte";

  import { Router, Link, Route } from "svelte-routing";

  export let url = "";
</script>

<style lang="scss" global>
  @import "./style/global.scss";
</style>

<Router {url}>

  <div>
    <Route path="/event" component={EventPage} />
    <Route path="/" exact>
      <HomePage />
    </Route>
  </div>
</Router>
