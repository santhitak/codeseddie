<script lang="ts">
  import Counter from './lib/Counter.svelte'
  import './lib/css/fontface.css'
</script>

<main>
  <h1>Hello Typescript!</h1>

  <Counter />
</main>

<style>

  :root {
    font-family: 'SQ Market', sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  h1 {
    color: #001aff;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 400;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }
  }
</style>
