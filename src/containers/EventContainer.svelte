<script>
  import Event from "../components/Event.svelte";

  let loader = true;
  setTimeout(generateData, 2000);
  async function generateData() {
    loader = false;
  }

  let data = [
    {
      name: "ACCATHON 2019",
      date: "12/12/12",
      timing: "HH:MM",
      venue: "Plot no. 9"
    },
    {
      name: "ACCATHON 2020",
      date: "12/12/12",
      timing: "HH:MM",
      venue: "Plot no. 9"
    },
    {
      name: "ACCATHON 2021",
      date: "12/12/12",
      timing: "HH:MM",
      venue: "Plot no. 9"
    },
    {
      name: "ACCATHON 2022",
      date: "12/12/12",
      timing: "HH:MM",
      venue: "Plot no. 9"
    }
  ];
</script>

<style>

</style>

<div>
  {#if !loader}
    {#each data as { name, date, timing, venue }, i}
      <Event {name} {date} {timing} {venue} />
    {/each}
  {:else}
    <img
      src="https://loading.io/spinners/typing/lg.-text-entering-comment-loader.gif"
      alt="" />
  {/if}

</div>
