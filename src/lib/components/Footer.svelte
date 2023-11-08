<script>
  import Headline from "./Headline.svelte";
  import links from "../../assets/links";
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
      {#each links as link}
        <a href="#/api/{link}">Api {link}</a>
      {/each}
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
