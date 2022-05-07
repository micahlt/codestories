<svelte:head>
  <title>codestories</title>
</svelte:head>
<div class="header">
  <h1>where your code matters</h1>
  <div class="cta">
    <a href="/waitlist" class="button primary">Join Waitlist</a>
    <a href="/login" class="button secondary">Log In</a>
  </div>
  <div class="floating-glow" />
</div>

<style>
  .header {
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
    user-select: none;
  }

  h1 {
    font-size: clamp(2rem, 10vw, 5em);
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

  .cta {
    display: flex;
    z-index: 1;
  }

  .button {
    color: white;
    text-decoration: none;
    padding: 0.7em 1.2em;
    border: 1px solid white;
    border-radius: 0.7em;
    margin-right: 1em;
    transition: 0.2s;
    position: relative;
  }

  .button:last-of-type {
    margin-right: 0;
  }

  .button.secondary:hover {
    background: white;
    color: black;
  }

  .button.primary {
    background: white;
    color: black;
  }

  .button.primary:before {
    content: '';
    height: calc(100% + 1px);
    width: calc(100% + 1px);
    background: linear-gradient(to bottom right, #f4e784, #f24389, #a478f1);
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: -1;
    border-radius: 0.7em;
    transition: 1s;
  }

  .button.primary:hover:before {
    opacity: 1;
    transition: 0.5s;
  }

  .button.primary:hover {
    background-color: transparent;
    border-color: transparent;
    color: white;
  }

  @media only screen and (max-width: 890px) {
    h2 {
      text-align: center;
    }

    nav {
      align-items: center;
      justify-content: center;
      padding-top: 1em;
    }

    .nav-links {
      display: none;
    }
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
