<script lang="ts">
      export let valor: string

      $: tamanhoFonte = valor.length > 20 ? 'pequena' : `s-${valor}`
</script>

<div class={`tela ${tamanhoFonte}`}>
        <span>{valor}</span>
</div>

<style>
  .tela {
    display: flex;
    flex: 1;
    justify-content: flex-end;
    align-items: center;
    padding: 0px 5px;
    font-size: 1.7rem;
    background-color: aliceblue;
    overflow: hidden;
    margin: 2px 1px;
    border-top-right-radius: 5px;
    border-top-left-radius: 5px;
  }

  .s-10 { font-size: 1.4rem;}
  .s-11 { font-size: 1.35rem;}
  .s-12 { font-size: 1.25rem;}
  .s-13 { font-size: 1.15rem;}
  .s-14 { font-size: 1.05rem;}
  .s-15 { font-size: 0.95rem;}
  .s-16 { font-size: 0.85rem;}
  .s-17 { font-size: 0.75rem;}
  .s-18 { font-size: 0.65rem;}
  .pequena { font-size: 0.6rem ;}
  </style>