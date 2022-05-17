<script>
  import Theme from "./Theme.svelte"
  import Card from "./Card.svelte"
  import Map from "./Map.svelte"
  import Phone from "./Phone.svelte"
  import HN from "./HN.svelte"
  import Footer from "./Footer.svelte"
  import JSConfetti from "js-confetti"

  if (typeof document != "undefined") {
    if (!localStorage.getItem("bud.returning-visitor")) {
      const jsConfetti = new JSConfetti()
      jsConfetti.addConfetti()
      localStorage.setItem("bud.returning-visitor", 1)
    }
  }
</script>

<Theme>
  <h1>Hey Bud 👋</h1>

  <p class="subheader">
    Thanks for checking out Bud! Learn more with the quick links below or create
    a root controller and index view to go on your own adventure.
  </p>

  <div class="cards">
    <Card href="https://www.youtube.com/watch?v=LoypcRqn-xA">
      <div class="card">
        <HN />
        <h2>Hacker News Demo <span class="arrow">→</span></h2>
        <p>
          Create your very own minimal Hacker News clone in 15 minutes with Bud.
        </p>
      </div>
    </Card>
    <Card
      href="https://denim-cub-301.notion.site/Hey-Bud-4d81622cc49942f9917c5033e5205c69"
    >
      <div class="card">
        <Map />
        <h2>Read the Docs <span class="arrow">→</span></h2>
        <p>
          Learn about all the things you can do with Bud in our comprehensive
          guide.
        </p>
      </div>
    </Card>
    <Card href="https://cal.com/mattmueller/30min">
      <div class="card">
        <Phone />
        <h2>Schedule a Quick Call <span class="arrow">→</span></h2>
        <p>
          For the more personal touch, jump on a call with Matt for questions
          and a demo.
        </p>
      </div>
    </Card>
  </div>

  <Footer />
</Theme>

<style>
  /* TODO: move to layout */
  :global(body) {
    font-size: 16px;
    --gray-50: #f8fafc;
    background-color: var(--gray-50);
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-rendering: optimizeLegibility;
  }

  h1 {
    margin-top: 160px;
    text-align: center;
    font: var(--display-487);
    letter-spacing: -0.02em;
  }

  .subheader {
    margin: 0 auto;
    text-align: center;
    color: var(--gray-600);
    font: var(--text-204);
    max-width: 675px;
  }

  .cards {
    list-style: none;
    display: flex;
    padding: 0 var(--size-32);
    gap: var(--size-32);
    max-width: 1400px;
    margin: var(--size-64) auto 0 auto;
  }

  .cards h2 {
    font: var(--text-206);
    color: var(--gray-700);
  }

  .card {
    padding: var(--size-32);
  }

  .card .arrow {
    visibility: hidden;
  }

  .card:hover .arrow {
    visibility: initial;
  }

  .cards p {
    font: var(--text-204);
    color: var(--gray-600);
  }
</style>
