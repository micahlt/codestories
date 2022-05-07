<script>
  let email = '';
  let isOnWaitlist = false;
  const siteKey = 'fBtUMeH0fL8Su421AANQpN97P8npV6dP';
  const handleSubmit = (e) => {
    e.preventDefault();
    Pageclip.send(siteKey, 'waitlist', { email }, (error, res) => {
      if (res.data == 'ok') {
        isOnWaitlist = true;
      }
    });
  };
</script>

<svelte:head>
  <title>codestories | join waitlist</title>
</svelte:head>
<div class="content">
  <h1>join waitlist</h1>
  {#if isOnWaitlist}
    <p>You're on the waitlist! Check your inbox and you may be invited to the alpha soon!</p>
  {:else}
    <div class="form">
      <input type="email" name="email" bind:value={email} placeholder="enter your email" />
      <button on:click={handleSubmit}><saco-icon name="arrow.long.right" /></button>
    </div>
  {/if}
  <div class="floating-glow" />
  <script src="https://s.pageclip.co/v1/pageclip.js" charset="utf-8"></script>
</div>

<style>
  .content {
    display: flex;
    background: black;
    min-height: 100vh;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-family: 'Plus Jakarta Sans', sans-serif;
    text-align: center;
    transform: translate(0, 0);
    position: relative;
    overflow-x: hidden;
  }

  h1 {
    font-size: clamp(2rem, 10vw, 3em);
    color: white;
    background: linear-gradient(to right, #f4e784, #f24389, #a478f1);
    background: -webkit-linear-gradient(to right, #f4e784, #f24389, #a478f1);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    max-width: 85vw;
    line-height: 0.9em;
    padding: 0.5em;
    z-index: 1;
    user-select: none;
  }

  .floating-glow {
    background: linear-gradient(to right, #f4e784, #f24389, #a478f1);
    background: -webkit-linear-gradient(to right, #f4e784, #f24389, #a478f1);
    height: 60vh;
    width: 70vh;
    max-width: 90vw;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 0;
    filter: blur(150px);
    opacity: 0.3;
    border-radius: 100%;
    animation: rotateforever 10s linear infinite forwards;
  }

  .form {
    width: 40rem;
    max-width: 85%;
    z-index: 1;
    display: flex;
    justify-content: center;
    height: 2.5em;
  }

  .form input[type='email'] {
    padding: 1em 1.2em;
    border-radius: 2em;
    border-style: none;
    outline: none;
    width: 30vw;
    min-width: 200px;
    font-family: inherit;
  }

  input::placeholder {
    font-family: 'Plus Jakarta Sans', sans-serif;
  }

  .form button {
    height: 2.5rem;
    width: 2.5rem;
    border-radius: 2.5em;
    border-style: none;
    margin-left: 0.5rem;
    display: block;
    cursor: pointer;
    background: linear-gradient(to bottom right, #f4e784, #f24389, #a478f1);
    background: -webkit-linear-gradient(to bottom right, #f4e784, #f24389, #a478f1);
  }

  button saco-icon {
    display: block;
    color: white;
  }

  @keyframes rotateforever {
    0% {
      transform: translate(-50%, -50%) rotate(0deg);
    }
    50% {
      transform: translate(-50%, -50%) rotate(180deg) scale(0.7);
    }
    100% {
      transform: translate(-50%, -50%) rotate(360deg);
    }
  }
</style>
