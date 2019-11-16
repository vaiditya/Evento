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
      src="https://www.google.com/url?sa=i&source=images&cd=&ved=2ahUKEwjFxM-Coe7lAhXIXSsKHfDLAqQQjRx6BAgBEAQ&url=https%3A%2F%2Fwpamelia.com%2Floading-animation%2F&psig=AOvVaw3vbc-BGj7Q3Qfv2CYIYPbS&ust=1573977433535933"
      alt="" />
  {/if}
</div>
