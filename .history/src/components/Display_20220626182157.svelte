<script lang="ts">
      export let valor: string
</script>

<div class="tela">
        <span>{valor}</span>
</div>

<style>
  .tela {
    display: flex;
    flex: 1;
    justify-content: flex-end;
    align-items: center;
    padding: 0px 5px;
    background-color: aliceblue;
    overflow: hidden;
  }
</style>