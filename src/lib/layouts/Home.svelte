<script lang="ts">
  import ModeToggle from "@components/ModeToggle.svelte";
  import NextButton from "@components/NextButton.svelte";
  import Tabs from "@components/Tabs.svelte";
</script>

<section>
  <Tabs />
  <ModeToggle />
  <div class="wrapper">
    <div class="container">
      <h1>ten days<br />of code<NextButton /></h1>
    </div>
  </div>
</section>

<style>
  h1 {
    margin: 0;
    padding: 0;
    font-size: 8rem;
    user-select: none;
  }
  @media only screen and (max-width: 812px) {
    h1 {
      font-size: 3rem;
    }
  }
  @media only screen and (max-width: 1024px) {
    h1 {
      font-size: 6rem;
    }
  }
</style>
