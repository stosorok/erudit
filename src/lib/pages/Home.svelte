<script>
  import HeroSlider from "../components/HeroSlider.svelte";
  import Logo from "../components/Logo.svelte";
  import Button from "../components/Button.svelte";
  import Headline from "../components/Headline.svelte";
</script>

<div class="hero">
  <div class="conteiner">
    <div class="row">
      <div class="hero-left">
        <div class="logo"><Logo width="70px" /></div>
        <div class="headline"><Headline>Erudit Sigafon</Headline></div>
        <div class="about">
          <p>Унікальний пристрій на ринку мобільних телефонів</p>
        </div>
        <div class="hero-buttons">
          <a href="#/info">
            <Button secondary>Про Сігафон</Button>
          </a>
          <a href="#/info">
            <Button>Придбати в 1 клік</Button>
          </a>
        </div>
      </div>
      <div class="hero-right">
        <HeroSlider />
      </div>
    </div>
  </div>
</div>

<style>
  .hero-buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .logo {
    margin-bottom: 50px;
  }
  .about {
    color: azure;
    margin-bottom: 50px;
  }

  .headline {
    margin-bottom: 50px;
  }
  .hero {
    padding-top: 64px;
    padding-bottom: 64px;
  }

  .hero.hero--second {
  }
  .hero.hero--third {
  }
  .conteiner {
    /* outline: 1px solid #234; */
    margin: 0 auto;
    max-width: 1240px;
    padding-inline: 32px;
  }
  .row {
    /* outline: 1px solid #234; */
    display: flex;
    flex-wrap: wrap;
    /* align-items: center; */
    justify-content: space-between;
    gap: 50px;
  }
  .hero-left {
    /* background: #234; */
    /* width: 540px; */
    /* height: 530px; */
    flex-grow: 1;
  }
  .hero-right {
    /* background: #0c0; */
    /* max-width: 550px; */
    /* margin: auto; */
    flex-basis: 40%;
    flex-grow: 1;
  }
</style>
