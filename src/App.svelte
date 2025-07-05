<script>
  import Header from "./lib/Header.svelte";
  import Nav from "./lib/Nav.svelte";
  import About from "./lib/About.svelte";
  import Passions from "./lib/Passions.svelte";
  import Contact from "./lib/Contact.svelte";
  import Timeline from "./lib/Timeline.svelte";
</script>

<svelte:head>
  <title>Kailyn Lau | Portfolio</title>
  <link
    rel="stylesheet"
    href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;700&display=swap"
  />
</svelte:head>

<Header
  name="Kailyn Lau"
  tagline="CS and Math Student @ Wellesley | Aspiring Software Engineer"
/>
<Nav />
<About />
<Passions />
<Timeline />
<Contact />



