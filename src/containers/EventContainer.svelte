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
      timing: "15:00",
      venue: "Plot no. 9, AccionLabs"
    },
    {
      name: "CHRISTMAS 2019",
      date: "25/12/2019",
      timing: "19:00",
      venue: "NORTH WING"
    },
    {
      name: "CSI Annual Meet",
      date: "27/12/2019",
      timing: "11:00",
      venue: "A, SOUTH WING"
    },
    {
      name: "NEW YEARS EVE",
      date: "31/12/2019",
      timing: "23:00",
      venue: "Plot no. 9"
    }
  ];
</script>

<style>

</style>

<div style="margin-top: 50px;"> 
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
