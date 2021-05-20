<script>
  let numbers = [1, 2, 3, 4];

  const handleClick = () => {
    numbers = [...numbers, numbers.length + 1];
  };
  $: sum = numbers.reduce((p, c) => p + c, 0);
</script>

<main>
  {numbers.join(' + ')} = {sum}
  <button on:click={handleClick}> Add one </button>
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
  }
</style>
