<script>
  export let siteLinks
</script>

<div class='nav-links'>
  { #each siteLinks as { text, href } }
    <a class='link' {href}>{text}</a>
  { /each }
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
    margin-left: 12px;
  }

  .link:last-child {
    font-weight: 700;
    background-color: var(--red);
    color: var(--white);
    margin-left: 38px;
    padding: 0 31px;
  }

  .link:last-child:hover {
    background-color: var(--dark-red);  
  }
  
  .link:last-child:active {
    background-color: var(--red);  
  }

  @media (max-width: 1200px) {
    .link {
      padding: 0 12px;
    }

    .link:last-child {
      margin-left: 20px;
      padding: 0 28px;
    }
  }
</style>