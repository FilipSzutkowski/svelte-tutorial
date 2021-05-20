<script>
  import Basic from './Basic.svelte';
  import SumNumbers from './SumNumbers.svelte';
</script>

<main>
  <Basic />
  <SumNumbers />
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }
</style>
