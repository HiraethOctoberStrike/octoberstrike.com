<script>
import MobileNav from "./MobileNav/MobileNav.svelte";
import NavLinks from "./NavLinks/NavLinks.svelte";

  const links = [
    {
      text: 'Mutual Aid',
      href: '/mutual-aid'
    }
  ]

  let w;
</script>

<nav bind:clientWidth={w} >
  <a href='/'>
    <div class='logo-placeholder'></div>
  </a>
  {#if w > 500}
    <NavLinks {links} />
  {:else}
    <MobileNav {links} />
  {/if}
</nav>

<style>
  nav {
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: 72px;
    padding: 0 165px;
    background-color: var(--black);
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.15);
  }

  .logo-placeholder {
    background-color: var(--medium-grey1);
    width: 221px;
    height: 27px;
  }

  @media (max-width: 1200px) {
    nav {
      padding: 0 80px;
    }
  }

  @media (max-width: 700px) {
    nav {
      padding: 0 20px;
    }
  }
  
  @media (max-width: 700px) {
    nav {
      padding: 0 40px;
    }
  }
</style>