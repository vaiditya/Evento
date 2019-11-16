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
      icons: "/images/seminar.svg",
      venue: "Plot no. 9, ACCIONLABS, MUMBAI",
      custclass: "black"
    },
    {
      name: "Annual Presentation 2019",
      date: "25/12/2019",
      timing: "19:00",
      icons: "/images/team.svg",
      venue: "C-88, NORTH WING, MUMBAI",
      custclass: "green"
    },
    {
      name: "CSI Meet",
      date: "27/12/2019",
      timing: "11:00",
      icons: "/images/code.svg",
      venue: "A-77, SOUTH WING, PUNE",
      custclass: "red"
    },
    {
      name: "NEW YEARS EVE",
      date: "31/12/2019",
      timing: "23:00",
      icons: "/images/music.svg",
      venue: "D-99, QUARTER DUBLIN CIRCLE, BANGALORE",
      custclass: "purple"
    }
  ];

  function createEvent() {
    window.location = "./createEvent";
  }
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
    <button on:click={createEvent}>CREATE</button>
  {:else}
    <img
      class="loader"
      src="https://loading.io/spinners/typing/lg.-text-entering-comment-loader.gif"
      alt="" />
  {/if}

</div>
