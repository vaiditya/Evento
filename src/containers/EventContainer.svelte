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
      venue: "Plot no. 9, AccionLabs",
      custclass: "black"
    },
    {
      name: "CHRISTMAS 2019",
      date: "25/12/2019",
      timing: "19:00",
      venue: "NORTH WING",
      custclass: "green"
    },
    {
      name: "CSI Annual Meet",
      date: "27/12/2019",
      timing: "11:00",
      venue: "A, SOUTH WING",
      custclass: "red"
    },
    {
      name: "NEW YEARS EVE",
      date: "31/12/2019",
      timing: "23:00",
      venue: "Plot no. 9",
      custclass: "purple"
    }
  ];
</script>

<style>

</style>

<div style="margin-top: 50px;"> 
  {#if !loader}
    {#each data as { name, date, timing, venue, custclass }, i}
      <Event {name} {date} {timing} {venue} {custclass} />
    {/each}
  {:else}
    <img
      src="https://loading.io/spinners/typing/lg.-text-entering-comment-loader.gif"
      alt="" />
  {/if}

</div>
