<script>
  export let siteLinks;
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
      {#each siteLinks as { text, href } }
        <a on:click={closeMenu} class='link' {href}>{text}</a>
      {/each}
    </div>
  {/if}
</div>

<style>
  button {
    padding: 10px;
    background-color: transparent;
    border: none;
    cursor: pointer;
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
    box-sizing: border-box;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
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

  .link:last-child {
    font-weight: 700;
    color: var(--red);
  }

  .link:hover {
    background-color: var(--lightest-grey);
  }

  .link:active {
    background-color: var(--light-grey);  
  }
</style>