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
    z-index: 5;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh;
    background-color: bisque;
    
    background-image: linear-gradient(to right, rgba(0,0,0,1), rgba(255,255,255,0)), url("/images/background-image.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .menu{
    width: 90%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: auto;
    padding: 20px 0px;
  }


  h1,h6{
    color: white;
  }



  @media screen and (max-width: 500px) {
  .headline {
    align-items: flex-end;
    padding: 12rem 0rem;
  }
  }
</style>