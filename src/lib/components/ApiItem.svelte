<script lang="ts">
  export let item: {
    name: string;
    description: string;
  } | null = null;
</script>

{#if item}
  <div style="margin-bottom: 60px;">
    <h3>{item.name}</h3>
    <p>{item.description}</p>
  </div>
{/if}
