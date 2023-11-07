<!-- <script>
    document.body.addEventListener('mousemove', e => {
	document.querySelector('.container').style.perspectiveOrigin = `${e.clientX}px ${e.clientY}px`;
})
</script> -->

<div class="animation-container">
  <div class="animation" />
</div>

<style>
  .animation-container {
    overflow: hidden;
    perspective: 777px;
    /* perspective-origin: 100vh 100vh; */
    transform-style: preserve-3d;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: orange;
  }

  .animation {
    transform: rotateX(24deg) rotateY(25deg);
    width: 25vh;
    height: 35vh;
    background-image: url(https://cdn11.bigcommerce.com/s-spem6oukby/images/stencil/1280x1280/products/123/436/2D__57497__49826.1681470474.jpg);
    background-size: 100% 100%;
    border-radius: 15px;
    transition: transform 2000ms, filter 2ms 100ms;
    filter: hue-rotate(0deg) drop-shadow(5px 30px 15px #cf8600);
  }

  .animation:hover {
    transform: rotateY(0deg) rotateX(0deg);
    filter: hue-rotate(360deg) drop-shadow(5px 30px 15px #cf8600) blur(11px);
  }
</style>
