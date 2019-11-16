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
  .form-wrap {
    border: 1px solid #ddd;
    width: 500px;
    margin: 50px auto;
    background: rgb(56, 58, 79);
    padding: 20px;
    border-radius: 18px;
    box-shadow: 4px 6px 10px 3px #474444;
  }
  input {
    border: none;
    margin-bottom: 10px;
    background: none;
    border-bottom: 2px solid #ddd;
    color: #fff;
    font-size: 30px;
  }
  label {
    font-weight: bold;
    margin-bottom: 10px;
    color: #fff;
  }
  div {
    display: flex;
    flex-direction: column;
  }
  .btn-wrap {
    display: inline-block;
    justify-content: space-around;
    width: auto;
    margin: 0 auto;
  }
  button.btn {
    background: #fff;
    border: 0;
    padding: 10px 20px;
    border-radius: 3px;
    margin: 10px;
  }
</style>

<div class="form-wrap">
  <div>
    <label>Event Title</label>
    <input placeholder="Title" />
  </div>
  <div>
    <label>Date</label>
    <input placeholder="Date" />

  </div>
  <div>
    <label>Timing</label>
    <input placeholder="Timing" />
  </div>
  <div>
    <label>Venue</label>
    <input placeholder="Venue" />
  </div>

  <div class="btn-wrap">
    <button class="btn">SAVE AS DRAFT</button>
    <button class="btn">PUBLISH</button>
  </div>
</div>
