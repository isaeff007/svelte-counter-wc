<svelte:options tag="count-btn" />

<script>
  import { onMount } from "svelte";
  export let count = 0;

  function onClick() {
    count = +count + 1;
  }
  onMount(() => {
    console.log("can use on mount");
  });
</script>

<button on:click={onClick}>Count {count}</button>

<style>
  button {
    width: 100px;
    height: 100px;
  }
</style>
