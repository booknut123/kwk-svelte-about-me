<script>
  let active = "about";

  const sections = ["about", "passions", "coding", "contact"];
</script>

<nav class="nav">
  <ul>
    {#each sections as section}
      <li>
        <a
          href={"#" + section}
          on:click={() => (active = section)}
          class:active={active === section}
          >{section.charAt(0).toUpperCase() + section.slice(1)}</a
        >
      </li>
    {/each}
  </ul>
</nav>

<style>
  .nav {
    background: white;
    border-bottom: 2px solid var(--accent);
    position: sticky;
    top: 0;
    z-index: 100;
  }

  .nav ul {
    display: flex;
    justify-content: center;
    gap: 2rem;
    list-style: none;
    margin: 0;
    padding: 1rem;
  }

  .nav a:hover {
    color: var(--jet);
    border-bottom: 2px solid var(--accent);
  }

  a.active {
    font-weight: bold;
    border-bottom: 2px solid var(--jet);
    color: var(--jet);
  }
</style>
