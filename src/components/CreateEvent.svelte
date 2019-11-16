<script>
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  let name = "";
  let date = "";
  let timing = "";
  let venue = "";

  function handleFormInput(e) {
    name = e.target.name === "name" ? e.target.value : name;
    date = e.target.name === "date" ? e.target.value : date;
    timing = e.target.name === "timing" ? e.target.value : timing;
    venue = e.target.name === "venue" ? e.target.value : venue;
  }
  function submitForm() {
    console.log(name, date, timing, venue);
    dispatch("submitForm", {
      name: name,
      date: date,
      timing: timing,
      venue: venue
    });
  }
</script>

<style>

</style>

<div>
  Name:
  <input name="name" on:input={handleFormInput} value={name} />
  Date:
  <input name="date" on:input={handleFormInput} value={date} />
  Timing:
  <input name="timing" on:input={handleFormInput} value={timing} />
  Venue:
  <input name="venue" on:input={handleFormInput} value={venue} />
  <button on:click={submitForm}>SUBMIT</button>
</div>
