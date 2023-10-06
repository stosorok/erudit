<script>
  import { onMount } from "svelte";
  import Splide from "@splidejs/splide";
  import "@splidejs/splide/css";

  onMount(() => {
    new Splide(".splide", {
      type: "loop",
    }).mount();
  });
</script>

<section class="splide">
  <div class="splide__track">
    <ul class="splide__list">
      <li class="splide__slide">
        <img src="https://i.ibb.co/mRQ00gH/image.png" alt="Сігафон" />
      </li>
      <li class="splide__slide">
        <img
          src="https://i.ibb.co/mRQ00gH/image.png"
          alt="Сігафон"
          style="transform: scaleX(-1);"
        />
      </li>
      <li class="splide__slide">
        <img
          src="https://i.ibb.co/mRQ00gH/image.png"
          alt="Сігафон"
          style="transform: scaleY(-1);"
        />
      </li>
    </ul>
  </div>
</section>
