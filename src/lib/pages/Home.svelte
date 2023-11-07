<script>
  import HeroSlider from "../components/HeroSlider.svelte";
  import Logo from "../components/Logo.svelte";
  import Button from "../components/Button.svelte";
  import Headline from "../components/Headline.svelte";
  import AboutInfo from "../components/AboutInfo.svelte";
  import AboutVideo from "../components/AboutVideo.svelte";
  import Footer from "../components/Footer.svelte";
</script>

<div class="hero">
  <div class="container">
    <div class="row">
      <div class="hero-left">
        <div class="logo"><Logo width="70px" /></div>
        <div class="headline"><Headline>Erudit Sigafon</Headline></div>
        <div class="hero-about">
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

<div class="about">
  <div class="container">
    <div class="row">
      <div class="about-video">
        <AboutVideo />
      </div>
      <div class="about-info">
        <AboutInfo />
      </div>
    </div>
  </div>
</div>

<Footer />

<style>
  .about {
    padding: 92px 0px;
  }

  .hero-buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .logo {
    margin-bottom: 50px;
  }
  .hero-about {
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

  .row {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 50px;
  }
  .hero-left {
    flex-grow: 1;
  }
  .hero-right {
    flex-basis: 40%;
    flex-grow: 1;
  }
</style>
