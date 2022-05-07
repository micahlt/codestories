<script context="module">
  export function load({ error, status }) {
    return {
      props: {
        status,
        error: error
      }
    };
  }
</script>

<script>
  export let status, error;
</script>

<div class="error">
  <h1>{status}</h1>
  <p>{error.message}</p>
  <a href="/">Go Home</a>
</div>

<style>
  .error {
    height: 100vh;
    width: 100%;
    background-color: black;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-family: 'Plus Jakarta Sans', sans-serif;
  }

  .error h1 {
    font-size: 3em;
  }

  a {
    color: white;
    text-decoration: none;
    padding: 0.7em 1.2em;
    border: 1px solid white;
    border-radius: 0.7em;
    transition: 0.2s;
    margin-top: 1rem;
    position: relative;
  }

  a:hover {
    background: white;
    color: black;
  }
</style>
