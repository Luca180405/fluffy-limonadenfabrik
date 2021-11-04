<script>
  import Icon from 'svelte-awesome';
  import { faBars } from "@fortawesome/free-solid-svg-icons/faBars";
</script>

<nav
  class="flex flex-wrap items-center justify-between w-full bg-gradient-to-r from-yellow-400 via-orange-500 to-red-500"
>
  <a class="flex flex-wrap" href="/">
    <img
      src="/img/orangejuice.png"
      alt="Fluffy Logo"
      width="65px"
      height="65px"
    />
    <h1 class="text-6xl fluffy">Fluffy</h1>
  </a>
  <input type="checkbox" id="click" class="hidden"/>
  <label for="click" class="menu-btn lg:hidden md:hidden">
    <Icon class="text-white cursor-pointer" data="{faBars}" />
  </label>
  <ul class="flex flex-wrap text-2xl list-none">
    <li>
      <a
        class="text-lg font-medium tracking-wider text-gray-200 no-underline rounded-md active:text-black active:bg-white hover:bg-white hover:text-black active"
        href="/Unternehmen">Das Unternehmen</a
      >
    </li>
    <li>
      <a
        class="text-lg font-medium tracking-wider text-gray-200 no-underline rounded-md active:text-black active:bg-white hover:bg-white hover:text-black"
        href="/Shop">Shop</a
      >
    </li>
    <li>
      <a
        class="text-lg font-medium tracking-wider text-gray-200 no-underline rounded-md active:text-black active:bg-white hover:bg-white hover:text-black"
        href="/Rezepte">Rezepte</a
      >
    </li>
    <li>
      <a
        class="text-lg font-medium tracking-wider text-gray-200 no-underline rounded-md active:text-black active:bg-white hover:bg-white hover:text-black"
        href="/Handelspartner">Handelspartner</a
      >
    </li>
    <li onclick="location.href='./cart';" class="cursor-pointer svg">
          <svg class="svg2" xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 24 24" fill="none" stroke="#E5E7EB" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 2L3 6v14c0 1.1.9 2 2 2h14a2 2 0 0 0 2-2V6l-3-4H6zM3.8 6h16.4M16 10a4 4 0 1 1-8 0"/></svg>
    </li>
  </ul>
</nav>

<style>    
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600;700&display=swap");
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Poppins", sans-serif;
  }
  nav {
    height: 80px;
    padding: 0 50px 0 100px;
  }

  nav ul li {
    margin: 0 5px;
  }
  nav ul li a {
    padding: 8px 15px;
    transition: all 0.3s ease;
  }

  @media (max-width: 1000px) {
    nav {
      padding: 0 40px 0 50px;
    }
  }
  @media (max-width: 920px) {
    nav .menu-btn i {
      display: block;
    }
    #click:checked ~ .menu-btn i:before {
      content: "\f00d";
    }
    nav ul {
      position: fixed;
      top: 80px;
      left: -100%;
      background: linear-gradient(to right, var(--tw-gradient-stops));
      z-index: 2;
      height: 100vh;
      width: 100%;
      text-align: center;
      display: block;
      transition: all 0.3s ease;
    }
    #click:checked ~ ul {
      left: 0;
    }
    nav ul li {
      width: 100%;
      margin: 40px 0;
    }
    nav ul li a {
      width: 100%;
      margin-left: -100%;
      display: block;
      font-size: 20px;
      transition: 0.6s cubic-bezier(0.68, -0.55, 0.265, 1.55);
    }
    #click:checked ~ ul li a {
      margin-left: 0px;
    }
    nav ul li a.active,
    nav ul li a:hover {
      background: none;
      color: rgba(229, 231, 235, var(--tw-text-opacity));
    }
  }

  .fluffy {
    position: relative;
    top: -6px;
    bottom: auto;
    font-family: Veggy;
  }
</style>
