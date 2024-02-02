<script lang="ts">
  export let valor: string

  $: tamanhoFonte = valor.length > 20 ? 'pequena' : `s-${valor.length}`
</script>

<div class={`tela ${tamanhoFonte}`}>
  <span>{valor}</span>
</div>

<style>
  .tela {
    background: #FFF;
    border-radius: .25rem;

    display: flex;
    justify-content: flex-end;
    align-items: center;
    overflow: hidden;
    
    padding: .25rem .5rem;
    min-height: 45px;
    
    font-size: 1.75rem;
  }

  .s-10 { font-size: 1.6rem; }
  .s-11 { font-size: 1.5rem; }
  .s-12 { font-size: 1.4rem; }
  .s-13 { font-size: 1.3rem; }
  .s-14 { font-size: 1.2rem; }
  .s-15 { font-size: 1.1rem; }
  .s-16 { font-size: 1.05rem; }
  .s-17 { font-size: 1rem; }
  .s-18 { font-size: .94rem; }
  .s-19 { font-size: .88rem; }
  .s-20 { font-size: .84rem; }

  .pequena { font-size: .625rem; }
</style>