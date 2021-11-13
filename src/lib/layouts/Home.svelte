<script lang="ts">
  import ModeToggle from "@components/ModeToggle.svelte";
  import NextButton from "@components/NextButton.svelte";
</script>

<section>
  <ModeToggle />
  <div class="wrapper">
    <div class="container">
      <h1>ten days of coding<NextButton /></h1>
    </div>
  </div>
</section>

<style>
  h1{
    margin: 0;
    padding: 0;
    font-size: 8rem;
  }
  :global(section){
    width: 100vw;
    height: 100vh;
  }
  :global(.wrapper){
    height: 100%;
    width: 100%;
    align-items: center;
    display: flex;
    justify-content: center;
  }
  .container{
    height: 75vh;
    width: 60vw;
    align-items: center;
    display: flex;
    justify-content: center;
  }
</style>
