<script>
  import { Swipe, SwipeItem } from "svelte-swipe";
  let autoplay = true;
  let delay = 2000; //ms
  let showIndicators = true;
  let transitionDuration = 1000; //ms

  function onCreateEvent() {
    window.location = "/event";
  }
</script>

<style lang="scss">
  h1 {
    color: purple;
  }
  .swipe-holder {
    height: 50vh;
    width: 100%;
    margin: 0 auto;
    text-align: center;
  }
  img {
    max-width: 100%;
    height: auto;
  }
  .slider-wrap {
    position: relative;
  }
  .btn-cust {
    width: auto;
    background: #ed8031;
    border-radius: 5px;
    padding: 15px 35px;
    position: absolute;
    bottom: 13%;
    left: 40%;
    z-index: 9999;
    color: #fff;
    font-size: 20px;
    text-transform: uppercase;
    font-weight: 600;
    border:none;
  }
</style>

<div class="slider-wrap">

  <div class="swipe-holder">
    <Swipe {showIndicators} {autoplay} {delay} {transitionDuration}>
      <SwipeItem>
        <img src="../../public/images/e1.jpg" alt="" />
      </SwipeItem>

      <SwipeItem>
        <img
          src="../../public/images/e2.jpg"
          alt="" />
      </SwipeItem>

      <SwipeItem>
        <img
          src="../../public/images/e3.jpg"
          alt="" />
      </SwipeItem>

      <SwipeItem>
        <img src="../../public/images/e4.jpg" alt="" />
      </SwipeItem>
    </Swipe>
  </div>
  <button href="/event" class="btn-cust" on:click={onCreateEvent}>
    Create Event
  </button>
</div>
