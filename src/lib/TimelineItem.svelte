<script>
  export let title = "";
  export let items = [];
</script>

<div class="timeline-item">
  {#if title}
    <h4>{title}</h4>
  {/if}
  <ul>
    {#each items as item}
      <li>{@html item}</li>
    {/each}
  </ul>
</div>

<style>
  .timeline-item {
    margin-bottom: 1.5rem;
  }

  h4 {
    margin: 0.5rem 0;
    font-weight: bold;
    color: var(--jet);
  }

  ul {
    padding-left: 1.5rem;
    margin: 0;
  }

  li {
    margin-bottom: 0.5rem;
  }
</style>
