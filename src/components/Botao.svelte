<script lang="ts">
  export let texto: string;
  export let triplo: boolean = false;
  export let duplo: boolean = false;
  export let botoes: boolean = false;
  export let operacao: boolean = false;
  export let destaque: boolean = false;
  export let onClick: (valor: string) => void = () => {}
</script>

<button
  class="botao"
  on:click={() => onClick(texto)}
  class:triplo
  class:duplo
  class:operacao
  class:destaque
  class:botoes
>
  {texto}
</button>

<style>
  .botao {
    display: flex;
    justify-content: center;
    align-items: center;

    color: #121214;
    border: none;

    border-radius: 0.5rem;
    margin: 0;

    font-size: 2rem;
    font-weight: 600;
    line-height: 156%;

    cursor: pointer;
    transition: all 0.2s ease;
  }

  .botoes:hover {
    background: #FFF5BD;
  }

  .operacao:hover {
    background: #FFBA3D;
  }

  .destaque:hover {
    background: #66BBD1;
  }

  .botoes {
    background: #fffadd;
  }

  .operacao {
    background: #ffcc70;
  }

  .destaque {
    background: #8ecddd;
  }
</style>
