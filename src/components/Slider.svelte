<script>
  import { Swipe, SwipeItem } from "svelte-swipe"; // gzipped 3.37 KB

  let autoplay = true;
  let delay = 2000; //ms
  let showIndicators = true;
  let transitionDuration = 1000; //ms
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
  }
</style>

<div class="slider-wrap">

  <div class="swipe-holder">
    <Swipe {showIndicators} {autoplay} {delay} {transitionDuration}>
      <SwipeItem>
        <img
          src="https://bigfday.com/blog/wp-content/uploads/2018/06/Corporate-Event-1.jpg"
          alt="" />
      </SwipeItem>

      <SwipeItem>
        <img
          src="https://www.cdacentre.com/wp-content/uploads/2017/10/event.jpg"
          alt="" />
      </SwipeItem>

      <SwipeItem>
        <img
          src="https://www.seniorarchitectural.co.uk/wp-content/uploads/2018/09/exhibitor-tips-build-show.jpg"
          alt="" />
      </SwipeItem>

      <SwipeItem>
        <img src="https://c.pxhere.com/photos/b8/7a/photo-55317.jpg!d" alt="" />
      </SwipeItem>
    </Swipe>
  </div>
  <a class="btn-cust">Create Event</a>
</div>
