<script>
  export let time;
  const dateObject = new Date(time * 1000); // unix time is seconds, not milliseconds
</script>

<text transform="rotate(90)">
  {dateObject.toLocaleString("en-us")}
</text>
