<script> 
  // Scroll spy is cobbled together from a couple of github repos (I googled "scrollspy svelte"),
  // Svelte documentation, and AI prompts when I didn't understand documentation.
  import { onMount } from "svelte";

  let active = "about";
  const sections = ["about", "passions", "coding"];

  onMount(() => {
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            active = entry.target.id;
          }
        });
      },
      {
        rootMargin: "0px 0px -50% 0px",
      }
    );

    for (const id of sections) {
      const el = document.getElementById(id);
      if (el) observer.observe(el);
    }

    return () => observer.disconnect();
  });
</script>

<nav class="nav">
  <ul>
    {#each sections as section}
      <li>
        <a href={"#" + section} class:active={active === section}
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
