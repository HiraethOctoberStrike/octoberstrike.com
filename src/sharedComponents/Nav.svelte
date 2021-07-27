<script>
  let navLinks = [
    {
      text: 'About',
      url: '/about'
    },
    {
      text: 'Get Involved',
      url: '/get-involved'
    },
    {
      text: 'Mutual Aid',
      url: '/mutual-aid'
    },
    {
      text: 'FAQ',
      url: '/faq'
    },

  ]
</script>

<nav>
  <a href='/'>
    <div class='logo-placeholder'></div>
  </a>
  <div class='nav-links'>
      { #each navLinks as { text, url }, i}
        <a href={url}>{text}</a>
      {/each}
      <a class='primary-link' href='/strike-with-us'>Strike with Us</a>
    </div>
</nav>

<style>
  nav {
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    flex-grow: 1;
    padding: 0 165px 0 179px;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.15);
  }

  .logo-placeholder {
    background-color: var(--medium-grey1);
    width: 221px;
    height: 27px;
  }

  .nav-links {
    display: flex;
    flex-direction: row;
  }

  a {
    display: flex;
    cursor: pointer;
    font-size: 16px;
    font-weight: 500;
    color: var(--darkest-grey);
    padding: 43px 25px 38px;
    text-align: center;
    text-decoration: none;
    transition: 0.1s ease-in;
  }

  a:hover {
    background-color: var(--lightest-grey);
  }

  a:active {
    background-color: var(--light-grey);
  }

  .primary-link {
    font-weight: 700;
    background-color: var(--red);
    color: var(--white);
    margin-left: 38px;
    padding: 43px 31px 38px;
  }

  .primary-link:hover {
    background-color: var(--dark-grey);  
  }
  
  .primary-link:active {
    background-color: var(--medium-grey1);  
  }
</style>