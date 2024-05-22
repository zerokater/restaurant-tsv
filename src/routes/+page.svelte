<!-- src/routes/YourPage.svelte -->
<script context="module">
    export async function preload() {
      try {
        const res = await fetch('/static/pizzen.json');
        const pizzen = await res.json();
        return {
          pizzen
        };
      } catch (error) {
        console.error('Error fetching pizzas:', error);
        return {
          error: "Error fetching pizzas"
        };
      }
    }
  </script>
  
  <script>
    export let pizzen;
  </script>
  
  <h1>Pizzen</h1>
  
  {#if pizzen}
    {#each pizzen as pizza}
      <div>
        <h2>{pizza.name}</h2>
        <p>Description: {pizza.description}</p>
        <p>Price: {pizza.price}</p>
      </div>
    {/each}
  {:else}
    <p>Hala ska piza njer</p>
  {/if}
  