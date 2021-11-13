<script>
  function toggle() {
    window.document.body.classList.toggle("dark-mode");
  }
  let visible;
</script>

<label class="switch">
  {#if visible}
    <p>dark mode</p>
  {:else}
    <p>light mode</p>
  {/if}
  <input type="checkbox" bind:checked={visible} on:click={toggle} />
  <div>
    <span />
  </div>
</label>

<style>
  :root {
    --line: #505162;
    --dot: #dddddd;
    --circle: #9ea0be;
    --duration: 0.3s;
    --text: #9ea0be;
  }
  .switch {
    cursor: pointer;
    position: fixed;
    top: 1.2rem;
    right: 3rem;
    transform: scale(0.7);
  }
  .switch input {
    display: none;
  }
  .switch input + div {
    position: relative;
  }
  .switch input + div:before,
  .switch input + div:after {
    --s: 1;
    content: "";
    position: absolute;
    height: 4px;
    top: 10px;
    width: 24px;
    background: var(--line);
    transform: scaleX(var(--s));
    transition: transform var(--duration) ease;
  }
  .switch input + div:before {
    --s: 0;
    left: 0;
    transform-origin: 0 50%;
    border-radius: 2px 0 0 2px;
  }
  .switch input + div:after {
    left: 28px;
    transform-origin: 100% 50%;
    border-radius: 0 2px 2px 0;
  }
  .switch input + div span {
    padding-left: 56px;
    line-height: 24px;
    color: var(--text);
  }
  .switch input + div span:before {
    --x: 0;
    --b: var(--circle);
    --s: 3px;
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    width: 24px;
    height: 24px;
    border-radius: 50%;
    box-shadow: inset 0 0 0 var(--s) var(--b);
    transform: translateX(var(--x));
    transition: box-shadow var(--duration) ease, transform var(--duration) ease;
  }
  .switch input + div span:not(:empty) {
    padding-left: 64px;
  }
  .switch input:checked + div:before {
    --s: 1;
  }
  .switch input:checked + div:after {
    --s: 0;
  }
  .switch input:checked + div span:before {
    --x: 28px;
    --s: 12px;
    --b: var(--dot);
  }
  :global(body.dark-mode) .switch input:checked + div span:before {
    --b: var(--gray);
  }
  @media only screen and (max-width: 812px) {
    .switch {
      position: absolute;
      top: 1.2rem;
      right: 1rem;
    }
    p {
      display: none;
    }
  }
  @media only screen and (max-width: 1024px) {
    p {
      font-size: 1.1rem;
    }
  }
</style>
