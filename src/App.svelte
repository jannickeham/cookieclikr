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
    <h1>CookieClickr</h1>
  </div>

  <div>
    <img
      src={cookieImg}
      on:click={handleClick}
      on:keydown={handleClick}
      alt="Cookie"
    />
  </div>
  <div>
    <h3>{counter}</h3>
  </div>
  <button on:click={resetClicks}>Reset</button>
</main>

<style>
</style>
