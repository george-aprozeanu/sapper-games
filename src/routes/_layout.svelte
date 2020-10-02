<script>
  export let segment
</script>

<style>
  :global(body) {
    margin: 0;
    font-family: system-ui, BlinkMacSystemFont, -apple-system, 'Segoe UI', Roboto, sans-serif;
    min-height: 100vh;
    background-color: white;
    color: #303030;
  }
  @media (prefers-color-scheme: dark) {
    :global(body) {
      background-color: #222;
      color: lightslategray;
    }
  }
</style>

<main>
  <slot />
</main>
