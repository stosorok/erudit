<script>
  import Headline from "./Headline.svelte";
</script>

<footer class="hero">
  <div class="container">
    <div class="links">
      <Headline>Навігація</Headline>
      <a href="#/info">Флекси від Ерудита</a>
      <a href="#/animation">Анімація карт на ховері</a>
    </div>

    <div class="links">
      <Headline style="min-width: 200px;">Навчаємось з Ерудитом</Headline>
      <a href="#/api/descriptions">Api descriptions</a>
      <a href="#/api/xhr">Api xhr</a>
      <a href="#/api/websockets">Api websockets</a>
      <a href="#/api/streams">Api streams</a>
      <a href="#/api/html">Api html</a>
      <a href="#/api/fullscreen">Api fullscreen</a>
      <a href="#/api/fetch">Api fetch</a>
      <a href="#/api/encoding">Api encoding</a>
      <a href="#/api/dom">Api dom</a>
      <a href="#/api/indexedDB">Api IndexedDB</a>
    </div>
  </div>
</footer>

<style>
  footer {
    padding: 92px 0;
  }

  .links {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  a {
    color: white;
    font-weight: 700;
    font-family: sans-serif;
    text-decoration: none;
    font-size: 12px;
  }

  .container {
    display: flex;
    gap: 64px;
    justify-content: center;
    flex-wrap: wrap;
  }
</style>
