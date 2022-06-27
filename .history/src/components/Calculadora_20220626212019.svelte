<script lang="ts">
import CalculadoraModel from "src/model/CalculadorModel";

import Botao from "./Botao.svelte";
import Display from "./Display.svelte";
import Linha from "./Linha.svelte";

let calc = new CalculadoraModel()

const numeroDigitado = (num: string) => calc = calc.numeroDigitado(num)
const pontoDigitado = () => calc = calc.pontoDigitado()
const limpar = () => calc = calc.limpar()

</script>
<div class="calculadora">
 <Display valor= {calc.valor} />
  <Linha >
    <Botao destaque triplo texto="AC" onClick={limpar} />
    <Botao operacao texto="/"/>
</Linha>    
  <Linha >
             <Botao texto="7" onClick={numeroDigitado} /> 
             <Botao texto="8" onClick={numeroDigitado} />
              <Botao texto="9" onClick={numeroDigitado} />
              <Botao operacao texto="*"/>
      </Linha>
      <Linha >
        <Botao texto="4" onClick={numeroDigitado} />
        <Botao texto="5" onClick={numeroDigitado} />
         <Botao texto="6" onClick={numeroDigitado} />
         <Botao operacao texto="+"/>
 </Linha>
 <Linha >
  <Botao texto="1" onClick={numeroDigitado} />
  <Botao texto="2"onClick={numeroDigitado} />
   <Botao texto="3" onClick={numeroDigitado} />
   <Botao operacao texto="-"/>
</Linha>
<Linha >
  <Botao duplo texto="0" onClick={numeroDigitado} />
  <Botao texto="," onClick={pontoDigitado} />
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