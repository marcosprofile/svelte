<script>
  import Botao from "./Botao.svelte";
  import Linha from "./Linha.svelte";
  import Tela from "./Tela.svelte";
</script>

<div class="calculadora">
  <Tela valor="123" />
  <Linha>
    <Botao texto="AC" triplo destaque />
    <Botao texto="/" operacao />
  </Linha>
  <Linha>
    <Botao texto="7" botoes />
    <Botao texto="8" botoes />
    <Botao texto="9" botoes />
    <Botao texto="*" operacao />
  </Linha>
  <Linha>
    <Botao texto="6" botoes />
    <Botao texto="5" botoes />
    <Botao texto="4" botoes />
    <Botao texto="+" operacao />
  </Linha>
  <Linha>
    <Botao texto="3" botoes />
    <Botao texto="2" botoes />
    <Botao texto="1" botoes />
    <Botao texto="-" operacao />
  </Linha>
  <Linha>
    <Botao texto="0" duplo botoes />
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
