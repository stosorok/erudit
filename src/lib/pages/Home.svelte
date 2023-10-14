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
          <Button secondary>Про Сігафон</Button>
          <Button>Придбати в 1 клік</Button>
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
    background: linear-gradient(129deg, #F782A4 11.86%, #FB8A83 95.39%);
    padding-top: 20px;
    padding-bottom: 35px;
  }
  .conteiner {
    /* outline: 1px solid #234; */
    margin: 0 auto;
    max-width: 800px;
    padding-inline: 32px;
  }
  .row {
    /* outline: 1px solid #234; */
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    gap: 50px;
  }
  .hero-left {
    /* background: #234; */
    /* width: 540px; */
    /* height: 530px; */
  }
  .hero-right {
    /* background: #0c0; */
    width: 320px;

  }
</style>
