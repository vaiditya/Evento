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
      date: "12/12/2019",
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
  .btn-cust {
    width: auto;
   box-shadow: 2px 2px 2px #201c28;
    border-radius: 5px;
    padding: 15px 35px;
    z-index: 9999;
    color: #fff;
    font-size: 20px;
    text-transform: uppercase;
    font-weight: 600;
    border: none;
        background: #383a4f;
}
</style>

  {#if !loader}
  <div style="margin-top: 50px;">
    {#each data as { name, date, timing, venue, custclass, icons }, i}
      <Event {name} {date} {timing} {venue} {custclass} {icons} />
    {/each}
    <div style="display:flex;justify-content:space-around;margin: 30px 0;"> 
    <button class="btn-cust" on:click={createEvent}>CREATE</button>
    </div>
    </div>
  {:else} 
  <div style="display: flex;justify-content: center;min-height:100vh;align-items: center;">
    <img
      class="loader"
      src="https://mir-s3-cdn-cf.behance.net/project_modules/disp/35771931234507.564a1d2403b3a.gif"
      alt="" />
      </div>
  {/if}


