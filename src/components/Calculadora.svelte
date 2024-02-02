<script lang="ts">
  import Botao from "./Botao.svelte";
  import Linha from "./Linha.svelte";
  import Tela from "./Tela.svelte";

  class Model {
    valor: string
    constructor(valor: string = "0") {
      this.valor = valor;
    }

    inc() {
      return new Model(`${parseInt(this.valor) + 1}`)
    }
  }

  let obj = new Model();

  function numeroDigitado(numero: string) {
    obj = obj.inc()
  }

</script>

<div class="calculadora">
  <Tela valor={obj.valor} />

  <Linha>
    <Botao texto="AC" triplo destaque />
    <Botao texto="/" operacao />
  </Linha>
  <Linha>
    <Botao texto="7" botoes onClick={numeroDigitado} />
    <Botao texto="8" botoes onClick={numeroDigitado} />
    <Botao texto="9" botoes onClick={numeroDigitado} />
    <Botao texto="*" operacao />
  </Linha>
  <Linha>
    <Botao texto="6" botoes onClick={numeroDigitado} />
    <Botao texto="5" botoes onClick={numeroDigitado} />
    <Botao texto="4" botoes onClick={numeroDigitado} />
    <Botao texto="+" operacao />
  </Linha>
  <Linha>
    <Botao texto="3" botoes onClick={numeroDigitado} />
    <Botao texto="2" botoes onClick={numeroDigitado} />
    <Botao texto="1" botoes onClick={numeroDigitado} />
    <Botao texto="-" operacao />
  </Linha>
  <Linha>
    <Botao texto="0" duplo botoes onClick={numeroDigitado} />
    <Botao texto="," botoes />
    <Botao texto="=" duplo destaque />
  </Linha>
</div>

<style>
  .calculadora {
    background: var(--bg-700);

    width: 160px;
    border-radius: 0.5rem;

    display: flex;
    flex-direction: column;
    gap: 4px;

    padding: 0.5rem;

    box-shadow: 0 0 12px #00000085;

    transform: scale(1.75);
  }
</style>
