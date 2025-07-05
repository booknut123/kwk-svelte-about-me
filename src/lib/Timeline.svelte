<script>
  import TimelineGroup from "./TimelineGroup.svelte";

  const groups = [
    {
      year: "Middle School",
      entries: [
        {
          items: [
            "Dabbled in coding using Python basics.",
            "Sparked an early curiosity in logic, syntax, and creative problem-solving.",
          ],
        },
      ],
    },
    {
      year: "Freshman Year (2020–2021)",
      entries: [
        {
          title: "Kode with Klossy Mobile App Camp – Swift, SwiftUI, XCode",
          items: [
            "Built Crochet Central, a prototype iOS app for crochet lovers.",
            "Learned conditionals, functions, arrays, loops, classes, storyboards, and segues.",
            "Gained experience using XCode and user-focused design tools.",
          ],
        },
        {
          title: "Intro to Computer Science (in school) – Python",
          items: [
            "Explored foundational concepts like algorithms and debugging.",
            "Experience was more rigid and theoretical compared to KWK, but taught me persistence.",
          ],
        },
      ],
    },
    {
      year: "Sophomore Year (2021–2022)",
      entries: [
        {
          title: "Kode with Klossy Web Dev Camp – HTML, CSS, JavaScript",
          items: [
            "Created ReadIt, a book lovers' site featuring forums, rec quizzes, and Google Maps API.",
            "Designed for accessibility, UI/UX, and user empowerment, helping to support small bookstores.",
          ],
        },
        {
          title: "AP Computer Science: A (in school) – Java",
          items: [
            "Learned Java and other OOP concepts, but faced a frustrating classroom culture, which shaped my passions for gender equity in tech and ethical software development spaces.",
          ],
        },
      ],
    },
    {
      year: "Junior Year (2022–2023)",
      entries: [
        {
          title:
            "Kode with Klossy Data Science Camp – SQL, Python, Google Sheets, Colab",
          items: [
            "Analyzed substance abuse data across countries.",
            "Visualized international trends and explored data storytlling.",
            "Applied ethical tech principles and tackled a real-world issue I care about.",
          ],
        },
        {
          title: "Advanced Java (Johns Hopkins CTY)",
          items: [
            "Deepened understanding of Java beyond school curriculum.",
            "Built multiple small-scale projects focusing on performance and logic.",
          ],
        },
      ],
    },
    {
      year: "Senior Year (2023–2024)",
      entries: [
        {
          items: [
            "Led my second year as president of the American Computer Science League (ACSL) club, mentoring classmates in topics like boolean algebra, number systems, and LISP.",
            "Grew into a more confident teacher, peer mentor, and advocate for inclusive CS.",
            "Took a step back from formal coding programs to reflect on my journey and next steps as a college undergraduate.",
          ],
        },
      ],
    },
    {
      year: "College: Wellesley (2023–Present)",
      entries: [
        {
          title: "Text Adventure Game (CS230X) – Java, yED",
          items: [
            "Built a data-structure-driven game with graphs, stacks, queues, and trees.",
            "Used OOP, gameplay mechanics, and custom maps.",
          ],
        },
        {
          title: '"Peckish" App (CS248) – Python, SQL, Pandas',
          items: [
            "Co-created a joyful, privacy-focused food journaling app with Streamlit.",
            "Pulled live dining hall data via WellesleyFresh API; added tagging and community features.",
            "Emphasized value-sensitive design, user trust, and community-centered UX.",
          ],
        },
        {
          title: "KWK Data Storytelling Challenge",
          items: ["Where we are now! 🎉"],
        },
      ],
    },
  ];
</script>

<section id="coding" class="section">
  <h2>My Coding Journey</h2>
  <div class="timeline">
    {#each groups as group}
      <TimelineGroup {...group} />
    {/each}
  </div>
</section>

<style>
  .timeline {
    /* Vertical line part */
    position: relative;
    max-width: 1200px;
    margin: 0 auto;
  }

  .timeline::after {
    /* Vertical line part */
    content: "";
    position: absolute;
    width: 6px;
    background-color: var(--jet);
    top: 0;
    bottom: 0;
    left: 5%;
  }
</style>
