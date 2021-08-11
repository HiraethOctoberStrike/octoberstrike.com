<script>
  import { fly, fade } from 'svelte/transition'
  
  export let title
  export let body

  let open = false
</script>

<div class='dropdown-card' 
  class:open
  in:fade
  on:click={() => { open = !open}}>
  <div class='title'>
    <h6>{title}</h6>
    <div class='icon-container'>
      <span class="iconify" data-icon="mdi-chevron-down"></span>
    </div>
  </div>
  {#if open}
    {#each body as paragraph}
      <p in:fly={{delay: 100, duration: 300, y: 10}}>{paragraph}</p>
    {/each}
  {/if}
</div>

<style>
  .dropdown-card {
    padding: 28px 42px;
    background-color: var(--lightest-blue);
    margin-bottom: 20px;
  }

  .title {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  .iconify {
    color: var(--bright-red);
    font-size: 36px;
    flex-shrink: 0;
  }
  
  .icon-container {
    transition: 0.1s ease-in;
  }

  .open .icon-container {
    transform: rotate(180deg);
  }

  p {
    /* display: none; */
    margin-top: 20px;
  }

  @media (max-width: 900px) {
    .dropdown-card {
      padding: 24px 20px;
      margin-bottom: 14px;
   }
  }
</style>