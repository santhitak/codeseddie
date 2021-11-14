<script>
  import * as animateScroll from "svelte-scrollto";

  export let showOnPx = 150;
  let hidden = true;

  function scrollContainer() {
    return document.documentElement || document.body;
  }

  function handleOnScroll() {
    if (!scrollContainer()) {
      return;
    }

    if (scrollContainer().scrollTop > showOnPx) {
      hidden = false;
    } else {
      hidden = true;
    }
  }
</script>

<svelte:window on:scroll={handleOnScroll} />

<div
  class="back-to-top"
  on:click={() => animateScroll.scrollToTop()}
  class:hidden
>
  <i class="mi mi-chevron-up"><span class="u-sr-only" /></i>
</div>

<style>
  .back-to-top {
    opacity: 1;
    transition: opacity 0.5s, visibility .8s;
    position: fixed;
    right: 5rem;
    bottom: 4rem;
    z-index: 99;
    user-select: none;
  }

  i {
    font-size: 2rem;
  }

  .back-to-top.hidden {
    opacity: 0;
    visibility: hidden;
  }
  @media only screen and (max-width: 812px) {
    .back-to-top {
      bottom: 1.2rem;
      right: 1.2rem;
    }
  }
</style>
