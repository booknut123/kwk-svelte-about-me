<script>
  import TimelineItem from "./TimelineItem.svelte";

  export let year = "";
  export let entries = []; // each entry: { title (optional), items: [...] }
</script>

<div class="container content">
  <h2>{year}</h2>
  {#each entries as entry}
    <TimelineItem {...entry} />
  {/each}
</div>

<style>
  .container {
    padding: 10px;
    position: relative;
  }

  .container::after {
    /* The circles on the timeline */
    content: "";
    position: absolute;
    width: 25px;
    height: 25px;
    left: 3.5%;
    background-color: white;
    border: 4px solid var(--jet);
    top: 40px;
    border-radius: 50%;
    z-index: 1;
  }

  .content {
    background-color: white;
    position: relative;
    border-radius: 6px;
  }

  .container {
    width: 90;
    padding-left: 10%;
  }
</style>
