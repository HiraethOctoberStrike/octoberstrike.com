<script>
  import { fly, fade } from 'svelte/transition'
  
  export let title
  export let body

  let open = false
</script>

<div class='dropdown-card' class:open in:fade>
  <div class='title' on:click={() => { open = !open }}>
    <h6>{title}</h6>
    <div class='icon-container'>
      <span class="iconify" data-icon="mdi-chevron-down"></span>
    </div>
  </div>
  {#if open}
    <div class='body'>
      {#each body as paragraph}
      <p in:fly={{delay: 100, duration: 300, y: 10}}>{@html paragraph}</p>
      {/each}
    </div>
  {/if}
</div>

<style>
  .dropdown-card {
    background-color: var(--light-blue);
    margin-bottom: 20px;
  }

  .title {
    padding: 28px 42px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    cursor: pointer;
  }

  .iconify {
    color: var(--light-red);
    font-size: 36px;
    flex-shrink: 0;
  }
  
  .icon-container {
    transition: 0.1s ease-in;
    margin-left: 20px;
  }

  .open .icon-container {
    transform: rotate(180deg);
  }

  .body {
    padding: 0px 42px 28px;
    margin-top: -28px;
  }

  p {
    margin-top: 24px;
  }

  @media (max-width: 900px) {
    .dropdown-card {
      margin-bottom: 14px;
   }

    .title {
      padding: 24px 20px;
    }

    .body {
      padding: 0px 20px 24px;
      margin-top: -24px;
    }
  }
</style>