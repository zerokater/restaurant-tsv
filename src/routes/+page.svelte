<script>
  import Section from "../components/Section.svelte";
  import Button from "../components/Button.svelte";
  import Menu from "../components/Menu.svelte";

</script>


<main class="headline">
  <Section>
    <h1>Schmecke die beste<br>Pizza und Pasta der Stadt</h1>
    <h6>Authentische Rezepte, frische<br>Zutaten, unvergleichlicher Geschmack</h6> 
    <Button link="#menu" buttonText="Menü Ansehen"/>
  </Section>
</main>


<main class="menu" id="menu">
  <Menu/>
</main>


<style>
  .headline{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh;
    background-color: bisque;
    
    background-image: linear-gradient(to right, rgba(0,0,0,1), rgba(255,255,255,0)), url("./images/background-image.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .menu{
    padding: 2rem;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .menu img{
    height: 100%;
  }


  h1,h6{
    color: white;
  }

</style>