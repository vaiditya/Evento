<script>
  import Event from "../components/Event.svelte";

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
  {#each data as { name }, i}
    <Event {name} />
  {/each}

</div>
