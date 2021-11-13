<svelte:head>
  <link
    rel="stylesheet"
    href="https://unpkg.com/mono-icons@1.0.5/iconfont/icons.css"
  />
</svelte:head>

<div class="wrapper">
  <div class="arrow">
    <i class="mi mi-arrow-right"><span class="u-sr-only" /></i>
  </div>
</div>

<style>
  .u-sr-only {
    margin: 0;
    padding: 0;
  }
  i{
    transition: .2s linear;
  }
  i:hover {
    margin-left: 1.5rem;
  }
  .wrapper {
    width: auto;
    height: auto;
    position: relative;
    display: inline-block;
    inline-size: auto;
    top: 35px;
  }
</style>
