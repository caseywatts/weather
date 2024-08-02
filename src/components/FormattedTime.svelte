<script>
  export let time;
  const dateObject = new Date(time * 1000); // unix time is seconds, not milliseconds
</script>

<time class="inline" datetime={dateObject.toISOString()}>
  {dateObject.toLocaleString("en-us")}
</time>
