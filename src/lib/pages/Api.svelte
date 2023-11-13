<script lang="ts">
  import links from "../../assets/links";
  import ApiItem from "../components/api/ApiItem.svelte";
  import ApiLink from "../components/api/ApiLink.svelte";
  import ApiSearch from "../components/api/ApiSearch.svelte";

  export let params: { wild: string };

  let items = [];
  let query = "";

  const fetchApi = async (apiType: string) => {
    const api = await import(`../../assets/api/${apiType}.json`);

    items = Object.entries(api.default).map(([key, value]) => ({
      name: key,
      description: value,
    }));
  };

  $: apiType = params.wild;
  $: fetchApi(apiType);
  $: filteredItems = items.filter(({ name }) =>
    name.toLowerCase().includes(query.toLowerCase())
  );
</script>

<div class="font-inter">
  <aside>
    {#each links as link}
      <ApiLink {link} active={link === apiType} />
    {/each}
  </aside>

  <main>
    <header>
      <h1>{apiType}</h1>
      <ApiSearch bind:query />
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
