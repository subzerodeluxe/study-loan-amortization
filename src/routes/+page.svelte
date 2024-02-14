<script>
  import Wizard from "./Wizard.svelte";
</script>

<svelte:head>
  <title>Bereken wanneer je je studielening hebt afbetaald</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
  <h1>Wanneer ben ik klaar met terugbetalen?</h1>
  <Wizard />
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex: 0.6;
  }

  h1 {
    width: 100%;
  }
</style>
