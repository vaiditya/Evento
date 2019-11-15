<script>
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();
  export let name;

  function getInput(e) {
    dispatch("message", {
      text: e.target.value
    });
  }
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<h1>
  {name}
  <input type="text" value={name} on:input={getInput} />
</h1>
