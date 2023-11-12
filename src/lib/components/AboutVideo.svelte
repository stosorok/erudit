<script>
  import src from "../../assets/video01.mp4";
</script>

<div class="video">
  <video {src} autoplay loop muted />
</div>

<style>
  video {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 50%;
  }
</style>
