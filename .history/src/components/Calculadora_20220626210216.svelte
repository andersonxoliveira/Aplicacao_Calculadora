<script lang="ts">
import CalculadoraModel from "src/model/CalculadorModel";

import Botao from "./Botao.svelte";
import Display from "./Display.svelte";
import Linha from "./Linha.svelte";

let calc = new CalculadoraModel()

</script>
<div class="calculadora">
 <Display valor= {calc.valor} />
  <Linha >
    <Botao destaque triplo texto="AC"/>
    <Botao operacao texto="/"/>
</Linha>    
  <Linha >
             <Botao texto="7" onClick={num => calc = calc.numeroDigitado(num)} />
             <Botao texto="8" onClick={num => calc = calc.numeroDigitado(num)} />
              <Botao texto="9" onClick={num => calc = calc.numeroDigitado(num)} />
              <Botao operacao texto="*"/>
      </Linha>
      <Linha >
        <Botao texto="4" onClick={num => calc = calc.numeroDigitado(num)} />
        <Botao texto="5" onClick={num => calc = calc.numeroDigitado(num)} />
         <Botao texto="6" onClick={num => calc = calc.numeroDigitado(num)} />
         <Botao operacao texto="+"/>
 </Linha>
 <Linha >
  <Botao texto="1" onClick={num => calc = calc.numeroDigitado(num)} />
  <Botao texto="2"onClick={num => calc = calc.numeroDigitado(num)} />
   <Botao texto="3" onClick={num => calc = calc.numeroDigitado(num)} />
   <Botao operacao texto="-"/>
</Linha>
<Linha >
  <Botao duplo texto="0" onClick={num => calc = calc.numeroDigitado(num)} />
  <Botao texto=","/>
   <Botao destaque texto="="/>
  </Linha>
</div>

<style>
      .calculadora {
        background-color: var(--cor-fundo);
        height:  220px;
        width:  150px;
        padding:  10px;
        border-radius:  10px;

        display: flex;
        flex-direction:  column;
      }
</style>