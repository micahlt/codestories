<svelte:head>
  <title>codestories | privacy</title>
</svelte:head>
<div class="content">
  <h1>privacy matters</h1>
  <p>
    Codestories is a personal project, and does not collect any data outside of what the user
    desires to input. There are no analytics plugins used on this site. The information on this page
    may be subject to change, and you are responsible for checking it regularly.
  </p>
  <div class="floating-glow" />
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

  p {
    width: 40rem;
    max-width: 85%;
    z-index: 1;
  }

  p a {
    color: inherit;
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
