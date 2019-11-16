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
  .loader {
    display: flex;
    left: 0;
    right: 0;
    position: fixed;
    z-index: 9999;
  }
</style>

<div>
  {#if !loader}
    <Slider />
    <Feature />
    <About />
    <Contact />
  {:else}
    <img
      class="loader"
      src="https://loading.io/spinners/typing/lg.-text-entering-comment-loader.gif"
      alt="loading.." />
  {/if}
</div>
