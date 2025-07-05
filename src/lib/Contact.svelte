<script>
  let email = "kailynmlau@gmail.com";
  let github = "https://github.com/booknut123";
  let linkedin = "https://www.linkedin.com/in/kailyn-lau-8b60a4333/";
</script>

<section id="contact" class="section contact">
  <h2>Contact Me</h2>
  <p>Want to collaborate, connect, or just say hi?</p>
  <a class="contact-link" href="mailto: {email}">Mail: kailynmlau@gmail.com</a>
  <a class="contact-link" href={linkedin} target="_blank"
    >LinkedIn: Kailyn Lau</a
  >
  <a class="contact-link" href={github} target="_blank">Github: booknut123</a>
</section>

<style>
  .contact-link {
    display: inline-block;
    background: var(--accent);
    color: white;
    padding: 0.75rem 1.5rem;
    border-radius: 25px;
    font-weight: bold;
    transition: background 0.3s ease;
  }

  .contact-link:hover {
    background: var(--jet);
  }
</style>
