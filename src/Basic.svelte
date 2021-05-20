<script>
  import Paragraph from './Paragraph.svelte';

  const name = '<strong>Filip</strong>';
  const src =
    'https://i.guim.co.uk/img/media/8a13052d4db7dcd508af948e5db7b04598e03190/0_294_5616_3370/master/5616.jpg?width=1200&height=1200&quality=85&auto=format&fit=crop&s=bcaa4eed2c1e6dab61c41a61e41433d9';
  let count = 0;
  const handleClick = () => {
    count += 1;
  };
  $: {
    if (count >= 20) count = 0;
    console.log('yo');
  }
</script>

<main>
  <h1>Hello {@html name.toLocaleUpperCase()}!</h1>
  <Paragraph />
  <img {src} alt="Cat" />
  <button on:click={handleClick}>
    Clicked {count}
    {count === 1 ? 'time' : 'times'}
    Doubled: {count * 2}
  </button>
</main>

<style>
  h1 {
    color: purple;
    font-size: 4em;
    font-weight: 100;
  }

  img {
    width: 400px;
  }
  button {
    margin: 1em;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
