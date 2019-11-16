<script>
  import Slider from "./Slider.svelte";
  import Feature from "./Feature.svelte";
  import About from "./About.svelte";
  import Contact from "./Contact.svelte";

  let loader = true;
  setTimeout(generateData, 2000);
  async function generateData() {
    loader = false;
  }
</script>

<style>

</style>

<div >
  {#if !loader}
    <Slider />
    <Feature />
    <About />
    <Contact />
  {:else}
  <div style="display: flex;justify-content: center;min-height:100vh;align-items: center;">
    <img
      class="loader"
      src="https://mir-s3-cdn-cf.behance.net/project_modules/disp/35771931234507.564a1d2403b3a.gif"
      alt="" />
      </div>
  {/if}
</div>
