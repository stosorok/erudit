<script>
  import Router from "svelte-spa-router";
  import Home from "./lib/pages/Home.svelte";
  import Info from "./lib/pages/Info.svelte";
  import Animation from "./lib/pages/Animation.svelte";

  const routes = {
    "/": Home,
    "/info": Info,
    "/animation": Animation,
  };
</script>

<svelte:head>
  <meta property="og:title" content="Erudit Sigafon" />
  <meta
    property="og:description"
    content="Вашій увазі неймовірний продукт який не має аналогів, перейдіть по посиланню та дізнайтесь більше"
  />
  <meta property="og:image" content="https://i.ibb.co/rkGyHfM/ew-2.png" />
  <meta property="og:url" content="erudit.com" />
  <meta property="og:type" content="website" />
</svelte:head>

<div class="app">
  <Router {routes} />
</div>
