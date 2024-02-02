<script lang="ts">
  export let quatro: boolean = false;
  export let tres: boolean = false;
  export let dois: boolean = false;

</script>

<div
  class="linha"
  class:quatro
  class:tres
  class:dois
>
  <slot />
</div>

<style>
  .linha {
    display: grid;
    gap: .5rem;
  }
  
  .quatro {
    grid-template-columns: repeat(4, 80px);
  }
  
  .tres {
    grid-template-columns: 168px 80px 80px;
  }
  
  .dois {
    grid-template-columns: 256px 80px;
  }
</style>