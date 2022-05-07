<nav>
  <a class="title" href="/"><h2>codestories</h2></a>
  <div class="nav-links">
    <a href="/about">About</a>
    <a href="/privacy">Privacy</a>
    <a href="#" class="login"><saco-icon name="person" /></a>
  </div>
</nav>

<style>
  nav {
    position: fixed;
    color: white;
    font-family: 'Plus Jakarta Sans', sans-serif;
    top: 0;
    left: 0;
    width: calc(100% - 16vw);
    z-index: 1;
    padding: 1vw 8vw;
    display: flex;
    user-select: none;
  }

  .title {
    flex-grow: 1;
    color: white;
    text-decoration: none;
  }

  .nav-links {
    display: flex;
    align-items: center;
  }

  .nav-links a {
    margin-left: 2em;
    color: white;
    text-decoration: none;
    position: relative;
  }

  .nav-links a:before {
    content: '';
    position: absolute;
    bottom: -0.15em;
    right: 0;
    width: 100%;
    height: 0.05em;
    max-width: 0;
    transition: 0.3s;
    background-color: white;
  }

  .nav-links a:hover:before {
    max-width: 100%;
  }

  .login {
    width: 20px;
    height: 20px;
    padding: 5px;
    padding-top: 5px;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 100%;
    background: linear-gradient(to bottom right, #f4e784, #f24389, #a478f1);
    transition: 0.2s;
  }

  .login saco-icon {
    transform: translateY(-1px);
  }

  .login:hover:before {
    max-width: 0 !important;
  }

  .login:hover {
    background: linear-gradient(to bottom right, #f4e784, #f24389, #a478f1);
  }

  @media only screen and (max-width: 890px) {
    .title,
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
</style>
