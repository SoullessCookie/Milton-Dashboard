<script>
  import { page } from "$app/stores";
  import logo from "$lib/images/milton.png";
  import github from "$lib/images/github.svg";
  import { onMount } from "svelte";

  let isSticky = false;

  onMount(() => {
    const navbar = document.querySelector(".navbar");
    const sticky = navbar.offsetTop;

    window.onscroll = () => {
      if (window.pageYOffset >= sticky) {
        navbar.classList.add("sticky");
      } else {
        navbar.classList.remove("sticky");
      }
    };
  });
</script>

<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Lilita+One&display=swap"
  rel="stylesheet"
/>

<header class="navbar">
  <div class="logo">
    <a href="https://milton-dashboard.wrigglysplash.repl.co">
      <img src={logo} alt="Milton" class="circular-image" />
      <span>Milton</span>
    </a>
  </div>
  <nav class="nav-links">
    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="/about">About</a></li>
      <li><a href="https://wrigglysplash.gitbook.io/milton-documentation/commands/moderation">Commands</a></li>
      <li><a href="/help">Help</a></li>
      <li><a href="/premium">Premium</a></li>
      <li><a href="/dashboard">Dashoard</a></li>
    </ul>
  </nav>
</header>

<style>
  .navbar {
    background-color: #272934;
    width: 100%;
    display: flex; /* Add display flex to align logo and links */
    justify-content: space-between; /* Align items to the left and right */
    align-items: center; /* Vertically align items */
    padding: 1rem;
    position: relative;
    z-index: 1000;
  }

  .navbar.sticky {
    position: fixed;
    top: 0;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }

  .logo {
    display: flex;
    align-items: center;
  }

  .logo a {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: white;
    font-family: "Lilita One", cursive;
  }

  .logo img {
    width: 40px;
    height: 40px;
    object-fit: cover;
    margin-right: 0.5rem;
  }

  .nav-links {
    padding: 1rem;
  }

  .nav-links ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex; /* Align links horizontally */
    margin-right: 2rem;
  }

  .nav-links li {
    margin-left: 1rem;
  }

  .nav-links a {
    text-decoration: none;
    transition: color 0.3s ease;
    color: white;
  }

  .nav-links a:hover {
    color: var(--color-theme-1);
  }
</style>
