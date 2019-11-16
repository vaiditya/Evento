<script>
  import Event from "../components/Event.svelte";

  let loader = true;
  setTimeout(generateData, 4000);
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
    {#each data as { name }, i}
      <Event {name} />
    {/each}
  {:else}
    <img
      src="https://i.pinimg.com/originals/39/ee/de/39eede5b8818d7c02d2340a53a652961.gif"
      alt="" />
  {/if}

</div>
