<script>
  export let weatherData = {};
    import FormattedTimeSVG from "./FormattedTimeSVG.svelte";
</script>

<div class="w-screen h-screen" style="height: 100vh;">
  <svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
    {#each weatherData.hourly.data as d, i}
      <g transform="translate({i*15}, 0)">
        <rect width="0.8rem" height="{(d.pressure - 1000)}rem" fill="blue"/>
        <FormattedTimeSVG time={d.time}/>
      </g>
      {/each}
  </svg>
</div>
