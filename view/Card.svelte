<script>
  export let href = ""
</script>

<a {href} class="card"><slot /></a>

<style>
  .card {
    display: block;
    text-decoration: none;
    background: var(--white);
    box-shadow: var(--shadow-medium);
    border-radius: var(--radius-8);
  }
  .card:hover {
    box-shadow: var(--shadow-small);
  }
</style>
