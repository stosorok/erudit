<script lang="ts">
  import { location } from "svelte-spa-router";
  import links from "../../assets/links";
  import ApiItem from "../components/api/ApiItem.svelte";
  import ApiLink from "../components/api/ApiLink.svelte";

  let items = [];
  let query = "";

  const fetchApi = async (apiType: string) => {
    const api = await import(`../../assets/api/${apiType}.json`);

    items = Object.entries(api.default).map(([key, value]) => ({
      name: key,
      description: value,
    }));
  };

  $: apiType = $location.split("/").pop();
  $: fetchApi(apiType);
  $: filteredItems = items.filter(({ name }) =>
    name.toLowerCase().includes(query.toLowerCase())
  );
</script>

<div>
  <aside>
    {#each links as link}
      <ApiLink {link} />
    {/each}
  </aside>

  <main>
    <header>
      <h1>{apiType}</h1>
      <input type="text" bind:value={query} placeholder="search" />
    </header>

    {#each filteredItems as item (item.name)}
      <ApiItem {item} />
    {/each}
  </main>
</div>

<style>
  :root {
    --api-dark: #2b2b2b;
  }
</style>
