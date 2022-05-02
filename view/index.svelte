<script>
  import Theme from "./Theme.svelte"
  import Card from "./Card.svelte"
  import Map from "./Map.svelte"
  import Phone from "./Phone.svelte"
  import HN from "./HN.svelte"
  import JSConfetti from "js-confetti"

  if (typeof document != "undefined") {
    const jsConfetti = new JSConfetti()
    jsConfetti.addConfetti()
  }
</script>

<Theme>
  <h1>👋 Welcome to Bud</h1>

  <p class="subheader">
    I'm just thrilled that you're trying out the beta version. Get started with
    the quick links below or simply create an index controller and view to go on
    your own adventure.
  </p>

  <div class="cards">
    <Card>
      <div class="card">
        <HN />
        <h2>Hacker News Demo <span class="arrow">→</span></h2>
        <p>
          Create your very own minimal Hacker News clone in 15 minutes with Bud.
        </p>
      </div>
    </Card>
    <Card>
      <div class="card">
        <Map />
        <h2>Read the Documentation <span class="arrow">→</span></h2>
        <p>
          Learn about all the things you can do with Bud in our comprehensive
          guide.
        </p>
      </div>
    </Card>
    <Card>
      <div class="card">
        <Phone />
        <h2>Schedule a 15 minute call <span class="arrow">→</span></h2>
        <p>
          For the more personal touch, jump on a call with Matt for questions
          and a demo.
        </p>
      </div>
    </Card>
  </div>

  <footer>
    <a href="/">Github</a>
    <a href="/">Twitter</a>
    <a href="/" class="version">Bud v0.0.2</a>
    <a href="/">Roadmap</a>
    <a href="/">Email</a>
  </footer>
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
    max-width: 850px;
  }

  .cards {
    list-style: none;
    display: flex;
    gap: 32px;
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
    display: none;
  }

  .card:hover .arrow {
    display: initial;
  }

  .cards p {
    font: var(--text-204);
    color: var(--gray-600);
  }

  footer {
    position: absolute;
    bottom: 0;
    right: 0;
    left: 0;
    padding: var(--size-16);
    text-align: center;
    z-index: -1;
  }

  footer a {
    color: var(--gray-400);
    text-decoration: none;
    padding: var(--size-32);
  }

  footer a:hover {
    text-decoration: underline;
  }

  footer .version {
    font-weight: bold;
  }
</style>
