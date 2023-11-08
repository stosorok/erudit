<script>
  import { location } from "svelte-spa-router";
  import { onMount } from "svelte";
  import { flip } from "svelte/animate";
  import { fade } from "svelte/transition";
  import ApiItem from "../components/ApiItem.svelte";

  const apiType = $location.split("/").pop();
  let apiMap = {};

  onMount(async () => {
    apiMap = (await import(`../../assets/api/${apiType}.json`)).default;
  });

  $: items = Object.entries(apiMap).map(([key, value]) => ({
    name: key,
    description: value,
  }));
</script>

<div>
  <h1>{apiType}</h1>

  {#each items as item (item.name)}
    <div in:fade animate:flip={{ duration: 200 }}>
      <ApiItem {item} />
    </div>
  {/each}
</div>
