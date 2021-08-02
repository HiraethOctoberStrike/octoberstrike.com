<script>
  const navLinks = [
    {
      text: 'Home',
      href: '/'
    },
    {
      text: 'Mutual Aid',
      href: '/mutual-aid'
    },
    {
      text: 'Strike with Us',
      href: '/strike-with-us'
    },
  ]

  const socialLinks = [
    {
      href: 'https://www.instagram.com/strikeoctober15/',
      src: 'assets/socialMediaLogos/instagram.png',
      alt: 'instagram'
    },
    {
      href: 'https://twitter.com/StrikeOctober',
      src: 'assets/socialMediaLogos/twitter.png',
      alt: 'twitter'
    },
    {
      href: 'https://www.facebook.com/strikeoctober15',
      src: 'assets/socialMediaLogos/facebook.png',
      alt: 'facebook'
    },
    {
      href: 'https://www.reddit.com/r/OctoberStrike/',
      src: 'assets/socialMediaLogos/reddit.png',
      alt: 'reddit'
    }
  ]
</script>

<footer>
  <div class='internal-links'>
    <a href='/'>
      <img src='assets/images/LMX_Logo_White.svg' />
    </a>
    <nav>
      { #each navLinks as { text, href } }
        <a class='internal-link' {href}>{text}</a>
      { /each }
    </nav>
  </div>
  <div class='social-links'>
      { #each socialLinks as { href, src, alt } }
        <a class='social-link' {href} target='_blank' >
          <img class='social-icon'{src} {alt} />
        </a>
      { /each }
  </div>
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

  .social-link {
    text-decoration: none;
  }

  .social-icon {
    height: 31px;
    width: 31px;
    border-radius: 16px;
    border: 1px solid var(--black);
    margin-right: 12px;
  }

  .social-icon:hover {
    border: 1px solid var(--light-grey);
  }

  .copyright-statement {
    color: var(--white);
    font-size: 16px;
    font-weight: 500;
    margin: 12px 0 0;
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