<!-- Not sure if I wanted to also make the bio a customizable param in App.svelte, so I just left it here... -->
<script>
  import photo from "./images/personal_photo.jpg";
</script>

<section id="about" class="section">
  <h2>About Me</h2>
  <div class="about-content">
    <img src={photo} alt="Kailyn" class="profile-img" />
    <div class="bio">
      <p>
        Hi! I'm Kailyn, a student at <a
          href="https://www.wellesley.edu"
          target="_blank">Wellesley College</a
        > ('28) from Southern California. I love merging creativity with technology
        — whether that’s through art, music, or software development.
      </p>
      <p>
        I'm looking to expand my knowledge and push boundaries! With a
        background in martial arts, music, and problem solving, I approach
        things from a unique place in life.
      </p>
    </div>
  </div>
</section>

<style>
  .about-content {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 2rem;
  }

  .profile-img {
    width: 200px;
    border-radius: 50%;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  }

  .bio {
    flex: 1;
  }
</style>
