<script>
  import Slider from "./Slider.svelte";
  import Feature from "./Feature.svelte";
  import About from "./About.svelte";
  import Contact from "./Contact.svelte";

  let loader = true;
  setTimeout(generateData, 4000);
  async function generateData() {
    loader = false;
  }
</script>

<style>

</style>

<div>
  {#if !loader}
    <Slider />
    <Feature />
    <About />
    <Contact />
  {:else}
    <img
      src="https://i.pinimg.com/originals/39/ee/de/39eede5b8818d7c02d2340a53a652961.gif"
      alt="" />
  {/if}
</div>
