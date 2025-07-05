<script>
  import { slide } from "svelte/transition";
  export let image, alt, title, description;
  let expanded = false;
  const toggle = () => (expanded = !expanded);
</script>

<div class="grid-item expandable-card">
  <img src={image} alt={alt || title} />
  <button class="card-title" on:click={toggle}>
    <h3>{title}</h3>
    <span class="arrow">{expanded ? "▲" : "▼"}</span>
  </button>
  {#if expanded}
    <div class="card-content" transition:slide>
      <p>{@html description}</p>
    </div>
  {/if}
</div>

<style>
  .grid-item {
    background: white;
    border-radius: 16px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    text-align: left;
    padding-bottom: 1%;
  }

  .grid-item:hover {
    transform: scale(1.02);
  }

  .grid-item img {
    width: 100%;
    height: 180px;
    object-fit: cover;
    border-top-left-radius: 16px;
    border-top-right-radius: 16px;
  }

  .card-title {
    background: none;
    border: none;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    padding: 1rem;
    font-size: 1rem;
    cursor: pointer;
  }

  .card-title h3 {
    margin: 0;
  }

  .card-content {
    overflow: hidden;
    transition:
      max-height 0.4s ease,
      padding 0.4s ease;
    padding: 0.5rem 1rem 1rem;
  }
</style>
