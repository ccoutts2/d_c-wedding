<script lang="ts">
    export let isOpen: boolean;
  </script>
  
  <section class="BurgerMenu" class:open={isOpen}>
    <h2>
      Clare and David's Wedding
    </h2>
    <menu>
      <li><a href='/'>Home</a></li>
      <li><a href='/'>Order of the day</a></li>
      <li><a href='/'>Travel</a></li>
      <li><a href='/'>Q & A</a></li>
    </menu>
  </section>
  
  <style>
    .BurgerMenu {
        background: rgba(255, 255, 255, 0.97);
      height: 100vh;
      left: 0;
      padding: 2rem 1rem;
      position: fixed;
      top: 0;
      width: 33%;
      clip-path: polygon(0 0, 100% 0, 100% 0, 0 0);
      transition: clip-path 0.5s ease-in-out;
      z-index: 9;
      overflow: hidden;
    }
  
    .BurgerMenu.open {
      clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
      
    }

    .BurgerMenu h2 {
        padding: 2.5rem 0;
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        font-style: italic;
        font-weight: 400;
        font-size: 2rem;
        line-height: 1.25;
        text-transform: none;
        letter-spacing: 0em;
        color: #358d90;
    }

    .BurgerMenu menu {
        margin: 0;
        padding: 0;
        list-style: none;
        color: black;
    }

    .BurgerMenu li {
       padding: 0.75rem 0;
       font-weight: 200;
    }

  </style>
  