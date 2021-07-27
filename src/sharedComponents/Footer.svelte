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
      <div class='logo-placeholder'></div>
    </a>
    <nav>
      { #each navLinks as { text, href } }
        <a class='internal-link' {href}>{text}</a>
      { /each }
    </nav>
  </div>
  <div class='social-links'>
      { #each socialLinks as { href, src, alt } }
        <a class='social-link' {href} target="_blank" >
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
    padding: 0 179px 0 165px;
  }

  .internal-links {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 45px 0 26px;
  }

  .logo-placeholder {
    background-color: var(--medium-grey1);
    width: 221px;
    height: 27px;
  }

  nav {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  
  .internal-link {
    padding: 0 45px;
  }

  a {
    color: var(--white);
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
    height: 80px;
    margin: 80px 0 0;
  }
</style>