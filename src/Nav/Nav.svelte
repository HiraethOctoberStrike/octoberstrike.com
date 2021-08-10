<script>
  import { siteLinks } from '../siteLinks.js'
  import MobileNav from "./MobileNav/MobileNav.svelte";
  import NavLinks from "./NavLinks/NavLinks.svelte";

  let w;
</script>

<nav bind:clientWidth={w} >
  <a href='/home'>
    <img src='assets/images/LMX_Logo_White_HALF.svg' alt='labor movement x logo'/>
    <p>Labor Movement X</p>
  </a>
  {#if w > 900}
    <NavLinks {siteLinks} />
  {:else}
    <MobileNav {siteLinks} />
  {/if}
</nav>

<style>
  nav {
    position: sticky;
    top: 0;
    z-index: 2;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: 72px;
    padding: 0 165px;
    background-color: var(--black);
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.15);
  }

  img {
    height: 56px;
    margin-right: 7px;
  }

  a {
    display: flex;
    flex-direction: row;
    align-items: center;
    flex-shrink: 0;
    text-decoration: none;
  }

  p {
    color: var(--white);
    font-size: 20px;
    font-weight: 400;
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
</style>