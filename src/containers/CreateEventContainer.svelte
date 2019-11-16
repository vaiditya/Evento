<script>
  import CreateEvent from "../components/CreateEvent.svelte";

  let loader = true;
  let name = "";
  let date;
  let timing;
  let venue;

  setTimeout(generateData, 2000);
  function generateData() {
    loader = false;
  }
</script>

<style>

</style>

<div>
  {#if !loader}
    <CreateEvent {name} {date} {timing} {venue} on:message:{handleFormInput} />
  {:else}
    <img
      src="https://loading.io/spinners/typing/lg.-text-entering-comment-loader.gif"
      alt="" />
  {/if}
</div>
