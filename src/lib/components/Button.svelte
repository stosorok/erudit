<script>
  export let secondary = false;
</script>

<button class="button {secondary ? 'secondary' : 'primary'}">
  <slot />
</button>

<style>
  .primary {
    background-color: rgba(254, 63, 63, 1);
    color: #fff;
    border-radius: 8px;
    border: 2px solid #fff;
    padding: 10px;
    min-height: 30px;
    min-width: 120px;
  }

  .primary:hover {
    background-color: rgba(217, 54, 54, 1);
    color: #fff;
    border-radius: 8px;
    border: 2px solid #fff;
    padding: 10px;
    min-height: 30px;
    min-width: 120px;
  }

  .primary:disabled {
    background-color: #343436;
    color: #fff;
    border: none;
    border-radius: 10px;
    padding: 15px;
    min-height: 30px;
    min-width: 120px;
  }

  .primary:active:not(:disabled) {
    background-color: #a32a2a;
    color: #fff;
    border-radius: 8px;
    border: 2px solid #fff;
    padding: 10px;
    min-height: 30px;
    min-width: 120px;
  }

  .secondary {
    background-color: rgba(0, 0, 0, 0);
    color: #fff;
    border-radius: 8px;
    border: 2px solid #fff;
    padding: 10px;
    min-height: 30px;
    min-width: 120px;
  }

  .secondary:hover {
    background-color: rgba(211, 24, 180, 0.1);
    color: #fff;
    border-radius: 8px;
    border: 2px solid #fff;
    padding: 10px;
    min-height: 30px;
    min-width: 120px;
  }

  .secondary:disabled {
    background-color: #343436;
    color: #fff;
    border: none;
    border-radius: 10px;
    padding: 15px;
    min-height: 30px;
    min-width: 120px;
  }

  .secondary:active:not(:disabled) {
    background-color: rgba(211, 24, 180, 0.8);
    color: #fff;
    border-radius: 8px;
    border: 2px solid #fff;
    padding: 10px;
    min-height: 30px;
    min-width: 120px;
  }
</style>
