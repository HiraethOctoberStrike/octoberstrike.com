<script>
  const navLinks = [
    {
      text: 'About',
      href: '/about'
    },
    {
      text: 'Get Involved',
      href: '/get-involved'
    },
    {
      text: 'Mutual Aid',
      href: '/mutual-aid'
    },
    {
      text: 'FAQ',
      href: '/faq'
    },
  ]
</script>

<nav>
  <a href='/'>
    <div class='logo-placeholder'></div>
  </a>
  <div class='nav-links'>
      { #each navLinks as { text, href } }
        <a class='link' {href}>{text}</a>
      { /each }
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
    height: 100px;
    padding: 0 179px 0 165px;
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
    align-items: center;
    text-decoration: none;
    transition: 0.1s ease-in;
  }

  a:hover {
    background-color: var(--lightest-grey);
  }

  a:active {
    background-color: var(--light-grey);
  }

  .link {
    font-size: 16px;
    font-weight: 500;
    color: var(--darkest-grey);
    padding: 0 25px;
    text-align: center;
  }

  .primary-link {
    font-weight: 700;
    background-color: var(--red);
    color: var(--white);
    margin-left: 38px;
    padding: 0 31px;
  }

  .primary-link:hover {
    background-color: var(--dark-grey);  
  }
  
  .primary-link:active {
    background-color: var(--medium-grey1);  
  }
</style>