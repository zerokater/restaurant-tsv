<script>
    import { onMount } from 'svelte';
    import { slide } from 'svelte/transition';
    let dropdownOpen = false;
  
    function toggleDropdown() {
      dropdownOpen = !dropdownOpen;
    }
  
    // Chiudere il dropdown menu quando si fa clic al di fuori di esso
    onMount(() => {
      function handleClick(event) {
        if (!event.target.closest('.dropdown')) {
          dropdownOpen = false;
        }
      }
      document.addEventListener('click', handleClick);
      return () => {
        document.removeEventListener('click', handleClick);
      };
    });
  </script>
  
  <header class="dropdown">
    <a href="{void(0)}" class="dropdown-toggle" on:click={toggleDropdown}>SPEISEKARTE</a>
    {#if dropdownOpen}
      <div class="dropdown-menu" transition:slide>
        <a href="/">Pizzen</a>
        <a href="/pasta">Pasta</a>
        <a href="/salate">Salate</a>
        <a href="/vorspeise">Vorspeise</a>
        <a href="/getranke">Getränke</a>
      </div>
    {/if}
  </header>
  
  <style>

    header{
      padding: 20px 0px;
    }

    .dropdown-toggle {
      display: flex;
      justify-content: center;
      border: 1pt solid black;
      color: #212529;
      padding: 24px;
      font-size: 32px;
      font-weight: 700;
      letter-spacing: 5px;
      cursor: pointer;
    }
  
    .dropdown-menu {
        display: flex;
        flex-direction: column;
      background-color: #ffffff;
      border: 1px solid #ced4da;
      min-width: 160px;
      z-index: 1;

    }
  
    .dropdown-menu a {
      padding: 8px 12px;
      color: #212529;
      text-decoration: none;
    }
  
    .dropdown-menu a:hover {
      background-color: #f8f9fa;
    }
  </style>
  