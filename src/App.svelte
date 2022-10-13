<script>
  import { scale } from "svelte/transition";
  import { quintOut } from "svelte/easing";

  let cookieImg = "./src/assets/cookie.png";

  let counter = 0;

  function handleClick() {
    counter++;
  }

  function resetClicks() {
    counter = 0;
  }
</script>

<main>
  <div>
    <img
      src={cookieImg}
      on:click={handleClick}
      on:keydown={handleClick}
      transition:scale={{
        duration: 500,
        delay: 500,
        opacity: 0.5,
        start: 0.5,
        easing: quintOut,
      }}
      alt="Cookie"
    />
  </div>
  <div>
    <p>{counter}</p>
  </div>
  <button on:click={resetClicks}>Reset</button>
</main>

<style>
</style>
