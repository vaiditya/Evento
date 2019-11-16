<script>
  export let name;
  export let date;
  export let timing;
  export let venue;
  export let custclass;
  export let icons;
</script>

<style lang="scss">
  .box-wrap {
    display: flex;
    justify-content: space-around;
  }
  .box {
    background: #201c29;
    color: #a1a1af;
    -webkit-box-shadow: 0 0 2rem #000;
    box-shadow: 0 0 2rem #000;
    width: 100%;
    margin: 0 10px;
    width: 90%;
    margin: 25px 10px;
    padding: 10px 20px;
    // display: flex;
  }
  .purple {
    background: #311e5e;
  }
  .red {
    background: #d12121;
  }
  .green {
    background: #0d4319;
  }
  span {
    margin: 0 20px 10px 0;
    padding-bottom: 10px;
  }
  h1 {
    padding: 10px 0;
    margin: 5px 0;
<<<<<<< HEAD
    // display: flex;
  }
  .mb-20 {
    margin-bottom: 20px;
=======
    color: #ffc;
>>>>>>> 513692bf1364f2dad661b08464c5e22b28515b10
  }
  .icons {
    // display: inline-flex;
    // justify-content: flex-end;
    text-align: right;
  }
  .venue {
    display: flex;
    justify-content: flex-end;
  }
</style>

<div class="box-wrap">
  <div class="box {custclass}">
    <h1>
      {name}
      <span>
        <img src={icons} class="icons" width="30px" height="30px" alt="icon" />
      </span>
    </h1>

    <div class="mb-20" style="justify-content:space-around;">
      <span>Date: {date}</span>
      <span>Timing: {timing}</span>
      <div class="mb-20 venue">Venue: {venue}</div>
    </div>

  </div>
</div>
