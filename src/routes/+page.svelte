<script>
  let pizzaOpen = false;

  import { slide } from "svelte/transition";
  function togglePizza(){
    pizzaOpen = !pizzaOpen;
  }
</script>

<main>
  <div class="pizza" >
    <div class="container-pizza">
      <h1>Pizzen</h1>
      <img src="/images/drop-down.svg" alt="" on:click={togglePizza}>
    </div>
    
      {#if pizzaOpen}
      <div class="pizzen" transition:slide>
        <p>margherita</p>
        <p>margherita</p>
        <p>margherita</p>
        <p>margherita</p>
        <p>margherita</p>
        <p>margherita</p>
        <p>margherita</p>
        <p>margherita</p>
        <p>margherita</p>
        <p>margherita</p>
        <p>margherita</p>
        <p>margherita</p>
      </div>
    {/if}

  </div>

  <h1>Pasta</h1>
  <h1>Salate</h1>
</main>
  



<style>


  main{
      padding: 1rem 0rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

  .pizza{
    display: flex;
    flex-direction: column;
    width: 100%;
    gap: 1rem;
  }

  .container-pizza{
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border: 1pt solid black;
  }

  .container-pizza img{
    width: 48px;

  }

  .pizzen{
    border: 1pt solid black;
    padding: 1rem;
  }



</style>