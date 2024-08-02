<script>
  export let weatherData = {};
    import FormattedTime from "./FormattedTime.svelte";
  import Formattedtime from "./FormattedTime.svelte";
</script>

<div class="w-screen h-screen" style="height: 100vh;">
  <svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
    {#each weatherData.hourly.data as d, i}
      <!-- <FormattedTime time={d.time} /> -->
      <rect width="0.8rem" height="{(d.pressure - 1000)}rem" fill="blue" x="{i*1}rem"/>
      {/each}
  </svg>
</div>
