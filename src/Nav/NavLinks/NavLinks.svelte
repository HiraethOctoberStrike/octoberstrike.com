<script>
  export let links
</script>

<div class='nav-links'>
  { #each links as { text, href } }
    <a class='link' {href}>{text}</a>
  { /each }
  <a class='primary-link' href='/strike-with-us'>Strike with Us</a>
</div>

<style>
  .nav-links {
    display: flex;
    flex-direction: row;
    height: 100%;
  }

  a {
    display: flex;
    align-items: center;
    text-decoration: none;
    transition: 0.1s ease-in;
  }

  a:hover {
    background-color: var(--dark-grey);
  }

  a:active {
    background-color: var(--medium-grey2);
  }

  .link {
    font-size: 16px;
    line-height: 20px;
    font-weight: 500;
    color: var(--white);
    padding: 0 25px;
    margin-left: 24px;
  }

  .primary-link {
    font-weight: 700;
    background-color: var(--red);
    color: var(--white);
    margin-left: 38px;
    padding: 0 31px;
  }

  .primary-link:hover {
    background-color: var(--bright-red);  
  }
  
  .primary-link:active {
    background-color: var(--light-red);  
  }

  @media (max-width: 1200px) {
    .link {
      padding: 0 12px;
    }

    .primary-link {
      margin-left: 20px;
      padding: 0 28px;
    }
  }
</style>