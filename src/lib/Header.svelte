<script>
  export let name;
  export let tagline;
</script>

<header class="welcome">
  <div class="welcome-text">
    <h1>{name}</h1>
    <p>{tagline}</p>
  </div>
</header>

<style>
  .welcome {
    position: relative;
    padding: 6rem 1rem;
    color: var(--jet);
    text-align: center;
  }

  .welcome::before {
    content: "";
    position: absolute;
    inset: 0;
    background: url("./images/santorini_landscape.jpg") center/cover
      no-repeat;
    opacity: 0.25;
    z-index: 0;
  }

  .welcome h1,
  .welcome p {
    position: relative;
  }
</style>
