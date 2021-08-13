<script>
  let rand = -1;

  function getRand() {
    fetch("./rand")
      .then((d) => d.text())
      .then((d) => (rand = d));
  }
</script>

<main>
  <h1>Random Number Generator</h1>
  <a href="https://yonah.ml">Yonah Aviv </a>
  <a href="https://github.com/y330/Flask-Svelte-Heroku-starter">
    <button>Github Repo</button></a
  >

  <span>This project is built with Flask, Svelte, Scss, and Heroku</span>

  <div class="card">
    <h2>Result</h2>
    Your number is: {rand}
    <br />
    <br />
    <button on:click={getRand}>Try again</button>
  </div>
</main>

<style lang="scss">
  main {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  }
  .card {
    width: 10em;
    border-radius: 10px;
    margin: 0.5em;
    color: white;
    font-weight: 400;
    padding: 0.25rem 2rem 5rem;
    background-color: #ff3d00;
  }
  button {
    background-color: #455;
    color: white;
    border: #455 solid 1px;
    border-radius: 10px;

    padding: 1em;
    transition: border-color 0.3s ease-in-out, background 0.2s ease-in-out;
    &:hover {
      background-color: #344;
    }
    &:active {
      background-color: #233;
      transform: scale(0.92);
    }
  }
</style>
