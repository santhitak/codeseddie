<script lang="ts">
  let count: number = 0
  const increment = () => {
    count += 1
  }
</script>

<button on:click={increment}>
  Clicks: {count}
</button>

<style>
  button {
    font-family: inherit;
    font-size: inherit;
    padding: 1em 2em;
    color: #001aff;
    background-color: rgba(0, 26, 255, 0.1);
    border-radius: 2em;
    border: 2px solid rgba(47, 0, 255, 0);
    outline: none;
    width: 200px;
    font-variant-numeric: tabular-nums;
    cursor: pointer;
  }

  button:hover {
    border: 2px solid #001aff;
  }

  button:active {
    background-color: rgba(0, 26, 255, 0.1);
  }

</style>
