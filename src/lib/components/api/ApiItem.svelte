<script lang="ts">
  import { fade } from "svelte/transition";

  export let item: {
    name: string;
    description: string;
  };
</script>

{#if item}
  <div in:fade>
    <span>{item.name}</span>
    <span>{item.description}</span>
  </div>
{/if}

<style>
  div {
    font-family: "DM Mono", monospace;
  }
</style>
