<script>
  export let links;
  let open = false;

  const toggleMenu = () => {
    open = !open
  }

  const closeMenu = () => {
    open = false
  }
</script>

<div class='hamburger-menu'>
  {#if open}
    <button on:click={toggleMenu}>
      <span class="iconify" data-icon="mdi-close"></span>
    </button>
  {:else}
    <button on:click={toggleMenu}>
      <span class="iconify" data-icon="mdi-hamburger-menu"></span>
    </button>
  {/if}

  {#if open}
    <div class='links'>
      <a on:click={closeMenu} class='link' href='/'>Home</a>
      {#each links as { text, href } }
        <a on:click={closeMenu} class='link' {href}>{text}</a>
      {/each}
      <a on:click={closeMenu} class='link primary-link' href='/strike-with-us'>Strike with Us</a>
    </div>
  {/if}
</div>

<style>
  button {
    padding: 10px;
    background-color: transparent;
    border: none;
  }
  .iconify {
    color: var(--white);
    font-size: 36px;
  }

  .links {
    position: absolute;
    display: flex;
    flex-direction: column;
    background-color: var(--white);
    top: 72px;
    padding: 20px;
    right: 0px;
    width: 100%;
  }

  .link {
    font-size: 16px;
    text-align: right;
    font-weight: 500;
    color: var(--black);
    padding: 18px 32px;
    text-decoration: none;
    transition: 0.1s ease-in;
  }

  .primary-link {
    font-weight: 700;
    color: var(--red);
  }

  .link:active {
    background-color: var(--white);  
  }
</style>