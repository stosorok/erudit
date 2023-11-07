<script>
  import { location } from "svelte-spa-router";
  import { onMount } from "svelte";

  const id = $location.split("/").pop();
  let apiMap = {};

  onMount(async () => {
    apiMap = (await import(`../../assets/api/${id}.json`)).default;
  });
</script>

<div>
  {#each Object.entries(apiMap) as [key, value]}
    <div>
      <h2>{key}</h2>
      <p style="margin-bottom: 40px;">{value}</p>
    </div>
  {/each}
</div>
