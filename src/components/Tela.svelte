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
    border-radius: .5rem;

    display: flex;
    justify-content: flex-end;
    align-items: center;
    overflow: hidden;
    
    padding: .25rem .5rem;
    min-height: 68px;
    
    font-size: 3.5rem;
  }

  .s-10 { font-size: 3.2rem; }
  .s-11 { font-size: 3rem; }
  .s-12 { font-size: 2.75rem; }
  .s-13 { font-size: 2.5rem; }
  .s-14 { font-size: 2.3rem; }
  .s-15 { font-size: 2.1rem; }
  .s-16 { font-size: 2rem; }
  .s-17 { font-size: 1.9rem; }
  .s-18 { font-size: 1.8rem; }
  .s-19 { font-size: 1.6rem; }
  .s-20 { font-size: 1.6rem; }

  .pequena { font-size: 1rem; }
</style>