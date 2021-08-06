<script>
import SocialLinks from "../sharedComponents/SocialLinks.svelte";

  const navLinks = [
    {
      text: 'Home',
      href: '/home'
    },
    {
      text: 'Mutual Aid',
      href: '/mutual-aid'
    },
    {
      text: 'Strike with Us',
      href: '/strike-with-us'
    },{
      text: 'FAQ',
      href: '/faq'
    },
  ]
</script>

<footer>
  <div class='internal-links'>
    <a href='/home'>
      <img src='assets/images/LMX_Logo_White-8.png' alt='a protest in grey-scale'/>
    </a>
    <nav>
      { #each navLinks as { text, href } }
        <a class='internal-link' {href}>{text}</a>
      { /each }
    </nav>
  </div>
  <a class='email' href='mailto: LaborMovementX@gmail.com'>LaborMovementX@gmail.com</a>
  <SocialLinks onDark/>
  <p class='copyright-statement'>Copyright © 2021 USA. All rights reserved.</p>
</footer>

<style>
  footer {
    background-color: var(--black);
    color: var(--white);
    padding: 44px 165px;
  }

  img {
    height: 150px;
  }

  .internal-links {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-start;
  }

  nav {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  
  .internal-link {
    padding: 0 45px;
    margin-bottom: 30px;
    text-decoration: none;
  }

  .internal-link:hover {
    text-decoration: underline;
  }
  
  a {
    color: var(--white);
    font-size: 16px;
  }

  p {
    color: var(--white);
    margin: 12px 0 8px;
  }

  .email {
    margin-bottom: 12px;
    display: inline-block;
    text-decoration: none;
  }

  .email:hover {
    text-decoration: underline;
  }
  
  .copyright-statement {
    font-size: 16px;
    font-weight: 500;
  }

  @media (max-width: 1100px) {
    footer {
      padding: 44px 80px;
    }
  }

  @media (max-width: 900px) {
    nav {
      flex-direction: column;
      align-self: flex-start;
    }

    .internal-link {
      text-align: right;
    }
  }
  
  @media (max-width: 700px) {
    footer {
      padding: 44px 40px;
    }
  }
  
  @media (max-width: 500px) {
    footer {
      padding: 44px 20px;
    }
  }
</style>