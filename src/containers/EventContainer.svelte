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
      custclass: "black",
      icons: "/images/seminar.svg"
    },
    {
      name: "Annual Presentation 2019",
      date: "25/12/2019",
      timing: "19:00",
      venue: "NORTH WING",
      custclass: "green",
      icons: "/images/team.svg"
    },
    {
      name: "CSI Meet",
      date: "27/12/2019",
      timing: "11:00",
      venue: "A, SOUTH WING",
      custclass: "red",
      icons: "/images/code.svg"
    },
    {
      name: "NEW YEARS EVE",
      date: "31/12/2019",
      timing: "23:00",
      venue: "Plot no. 9",
      custclass: "purple",
      icons: "/images/music.svg"
    }
  ];
</script>

<style>
  .loader {
    display: flex;
    justify-content: flex-end;
  }
</style>

<div style="margin-top: 50px;">
  {#if !loader}
    {#each data as { name, date, timing, venue, custclass, icons }, i}
      <Event {name} {date} {timing} {venue} {custclass} {icons} />
    {/each}
  {:else}
    <img
      class="loader"
      src="https://loading.io/spinners/typing/lg.-text-entering-comment-loader.gif"
      alt="" />
  {/if}

</div>
