<script>
  import "@fontsource/raleway"; // Defaults to weight 400
  import Header from "./Header.svelte";
</script>

<div class="app">
  <Header />
  <main>
    <slot />
  </main>

  <footer>
    <p>Made with love by Maarten and Sasi</p>
  </footer>
</div>

<style>
  :global(body) {
    --color-bg-0: rgb(202, 216, 228);
    --color-bg-1: hsl(209, 36%, 86%);
    --color-bg-2: hsl(224, 44%, 95%);
    --color-theme-1: #ff3e00;
    --color-theme-2: #4075a6;
    --color-text: rgba(0, 0, 0, 0.7);
    --column-width: 42rem;
    --column-margin-top: 4rem;
    color: var(--color-text);

    font-family: "Raleway";
    min-height: 100vh;
    margin: 0;
    background-attachment: fixed;
    background-color: var(--color-bg-1);
    background-size: 100vw 100vh;
    background-image: radial-gradient(50% 50% at 50% 50%, rgba(255, 255, 255, 0.75) 0%, rgba(255, 255, 255, 0) 100%),
      linear-gradient(180deg, var(--color-bg-0) 0%, var(--color-bg-1) 15%, var(--color-bg-2) 50%);
  }

  .app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  main {
    flex: 1;
    display: flex;
    flex-direction: column;
    padding: 1rem;
    width: 100%;
    max-width: 64rem;
    margin: 0 auto;
    box-sizing: border-box;
  }

  footer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 12px;
  }

  @media (min-width: 480px) {
    footer {
      padding: 12px 0;
    }
  }
</style>
