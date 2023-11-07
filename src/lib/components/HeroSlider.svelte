<script>
  // @ts-nocheck
  import { onMount } from "svelte";
  import Splide from "@splidejs/splide";
  import "@splidejs/splide/css";

  let slider;
  let hero;

  const arrowSVG = `
  <svg
  viewBox="0 0 100 47"
  fill="none"
  xmlns="http://www.w3.org/2000/svg"
  style="transform: scale(1); width: 100%; height: 100%;"
>
  <path
    d="M99.6052 9.91404L87.8643 32.9569L84.1635 26.1969L88.8396 22.8235L81.5322 10.4806L99.6055 9.91357L99.6052 9.91404ZM77.8329 10.5967L84.5253 21.9006L79.9285 25.2171L86.0814 36.4561L84.2878 39.9762L75.7043 39.1756L68.3371 25.7196L73.0134 22.3459L66.2716 10.9597L77.8327 10.5972L77.8329 10.5967ZM62.5728 11.0757L68.6995 21.4233L64.1023 24.7395L71.807 38.8123L57.1035 37.4408L50.8062 25.9388L55.4824 22.5652L48.9333 11.5034L62.5731 11.0756L62.5728 11.0757ZM40.2869 0.492169L40.2312 11.7766L45.2344 11.6195L51.168 21.6422L46.5709 24.9585L53.2058 37.0772L40.8545 35.9251L34.5418 24.395L39.2179 21.0209L30.3529 6.04755L40.2869 0.491784L40.2869 0.492169ZM27.5225 7.63107L34.9038 20.0983L30.3069 23.4146L40.0848 41.2748L40.0569 46.9516L25.4761 38.1745L17.4489 23.5127L22.1252 20.139L17.9043 13.01L27.5225 7.63107ZM15.0738 14.5929L17.8108 19.2163L13.2141 22.5328L19.9592 34.8534L0.159466 22.9343L15.0738 14.5929Z"
    fill="white"
    fill-opacity="0.6"
  />
</svg>`;

  const swapClass = (el, oldClass, newClass) => {
    if (oldClass) {
      el.classList.remove(oldClass);
    }

    el.classList.add(newClass);
  };

  onMount(() => {
    hero = document.querySelector("[id='app']");

    swapClass(hero, "", "hero--first");

    const splideEl = new Splide(".splide", {
      type: "loop",
    }).mount();

    splideEl.on("move", (index) => {
      const className =
        index === 0
          ? "hero--first"
          : index === 1
          ? "hero--second"
          : "hero--third";

      hero.classList.remove("hero--first", "hero--second", "hero--third");
      swapClass(hero, "", className);
    });

    setTimeout(() => {
      slider.querySelector(".splide__arrow--prev").innerHTML = arrowSVG;
      slider.querySelector(".splide__arrow--next").innerHTML = arrowSVG;
    }, 0);
  });
</script>

<svelte:body class="body" />

<section class="splide" bind:this={slider}>
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
