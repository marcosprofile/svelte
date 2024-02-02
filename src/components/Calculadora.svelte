<script lang="ts">
  import CalculadoraModel from "../model/CalculadoraModel";
  import Botao from "./Botao.svelte";
  import Linha from "./Linha.svelte";
  import Tela from "./Tela.svelte";

  let calc = new CalculadoraModel()

  const numeroDigitado = (num: string) => calc = calc.numeroDigitado(num)
  const operacaoDigitada = (op: string) => calc = calc.operacaoDigitada(op)
  const calcular = () => calc = calc.calcular()
  const virgulaDigitada = () => calc = calc.virgulaDigitada()
  const limpar = () => calc = calc.limpar()

</script>

<div class="calculadora">
  <Tela valor={calc.valor} />

  <Linha dois>
    <Botao texto="AC" triplo destaque onClick={limpar} />
    <Botao texto="/" operacao onClick={operacaoDigitada} />
  </Linha>
  <Linha quatro>
    <Botao texto="7" botoes onClick={numeroDigitado} />
    <Botao texto="8" botoes onClick={numeroDigitado} />
    <Botao texto="9" botoes onClick={numeroDigitado} />
    <Botao texto="*" operacao onClick={operacaoDigitada} />
  </Linha>
  <Linha quatro>
    <Botao texto="4" botoes onClick={numeroDigitado} />
    <Botao texto="5" botoes onClick={numeroDigitado} />
    <Botao texto="6" botoes onClick={numeroDigitado} />
    <Botao texto="+" operacao onClick={operacaoDigitada} />
  </Linha>
  <Linha quatro>
    <Botao texto="1" botoes onClick={numeroDigitado} />
    <Botao texto="2" botoes onClick={numeroDigitado} />
    <Botao texto="3" botoes onClick={numeroDigitado} />
    <Botao texto="-" operacao onClick={operacaoDigitada} />
  </Linha>
  <Linha tres>
    <Botao texto="0" duplo botoes onClick={numeroDigitado} />
    <Botao texto="," botoes onClick={virgulaDigitada} />
    <Botao texto="=" duplo destaque onClick={calcular} />
  </Linha>
</div>

<style>
  .calculadora {
    background: var(--bg-700);

    border-radius: 1rem;

    display: flex;
    flex-direction: column;
    gap: .5rem;

    padding: 1.25rem;

    box-shadow: 0 0 12px #00000085;
  }

  @media (max-width: 600px) {
		.calculadora {
      transform: scale(.75)
		}
	}
</style>
