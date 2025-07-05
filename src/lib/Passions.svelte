<script>
  import PassionCard from "./PassionCard.svelte";
  import TKD from "./images/tkd.png";
  import Cube from "./images/rubiks-cube.jpg";
  import Concert from "./images/concert.jpg";
  import Crochet from "./images/crochet.jpg";

  const cards = [
    {
      image: TKD,
      alt: "Tae Kwon Do",
      title: "Martial Arts",
      description:
        "I’ve practiced Tae Kwon Do for over eight years, with six years experience as a Taekwondo instructor. It’s taught me discipline, strength, and confidence, and as a second dan black belt, I strive to be a good role model for all of the children I'm mentoring. Aside from Tae Kwon Do, I've explored Shotokan Karate, Kickboxing, Taekwon-Do (ITF), and Kung Fu.",
    },
    {
      image: Cube,
      alt: "Rubik's Cube",
      title: "Speedcubing",
      description:
        "I love logic puzzles, whether pencil or other. My 3x3 Rubik's Cube record is 9.582 seconds, but I'm constantly working to improve! I don't compete often, but you can find me at <a href='https://www.worldcubeassociation.org/persons/2015LAUK01' target='_blank'>Kailyn Lau | WCA</a>.",
    },
    {
      image: Concert,
      alt: "Concert",
      title: "Music",
      description:
        "Music is a long-time passion of mine! I've seriously played (to varying degrees of success) over 15 instruments, but currently I'm focusing on piano, guzheng, carillon, and taiko drumming. My music tastes vary wildly, but my most common genres currently are k-pop, cantopop, and country, and I love attending concerts. I don't often perform, but make sure to check out <a href='https://www.youtube.com/@wellesleyaiko9187' target='_blank'>Wellesley Aiko</a> (our spring show <em>Echoes</em> was amazing, if I do say so myself)!",
    },
    {
      image: Crochet,
      alt: "Crocheting",
      title: "Yarn Crafts",
      description:
        "Fiber arts is so calming for me... I'm still exploring, but I picked up crocheting first and recently started tatting! Some might say my yarn stash is much bigger than it needs to be, although I'll never admit it. Knitting is next to tackle on my list, and then perhaps bobbin lace?",
    },
  ];
</script>

<section id="passions" class="section">
  <h2>Passions</h2>
  <div class="grid-container">
    {#each cards as card}
      <PassionCard {...card} />
    {/each}
  </div>
</section>

<style>
  .grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 24px;
    align-items: start;
  }
</style>
