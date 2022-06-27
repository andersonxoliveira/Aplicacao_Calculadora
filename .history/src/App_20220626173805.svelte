<script lang="ts">
import Calculadora from "./components/Calculadora.svelte";


</script>

<main>
        <Calculadora />
</main>

<style>
  :root {
    cor-fundo: #555 ;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
   display: flex;
   justify-content: center;
   align-items: center;
   height:  100vh;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

</style>
