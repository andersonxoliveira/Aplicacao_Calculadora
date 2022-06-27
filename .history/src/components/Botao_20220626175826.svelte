<script lang="ts">
      export let texto: string
      export let triplo: boolean = false
</script>

<button class= "botao" class:triplo>
{texto}
</button>

<style>
        .botao {
              flex-basis:  25%;
        }

          .triplo {
            flex-basis:  75%;
          }
</style>