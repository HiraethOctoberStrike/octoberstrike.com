<script>
  export let onDark = false;

  const socialLinks = [
    {
      href: 'https://www.instagram.com/labormovementx/',
      src: 'assets/socialMediaLogos/instagram.png',
      alt: 'instagram logo'
    },
    {
      href: 'https://twitter.com/laborMovementX',
      src: 'assets/socialMediaLogos/twitter.png',
      alt: 'twitter logo'
    },
    {
      href: 'https://www.tiktok.com/@labormovementx?',
      src: 'assets/socialMediaLogos/tiktok.png',
      alt: 'tiktok logo'
    },
    {
      href: 'https://www.facebook.com/strikeoctober15',
      src: 'assets/socialMediaLogos/facebook.png',
      alt: 'facebook logo'
    },
    {
      href: 'https://www.reddit.com/r/labormovementx/',
      src: 'assets/socialMediaLogos/reddit.png',
      alt: 'reddit logo'
    },
    {
      href: 'https://labormovementx.tumblr.com/',
      src: 'assets/socialMediaLogos/tumblr.png',
      alt: 'tumblr logo'
    },
    {
      href: 'https://discord.gg/YUvMTatzYC',
      src: 'assets/socialMediaLogos/discord.png',
      alt: 'discord logo'
    },
  ]
</script>

<div class='social-links' class:on-dark={onDark}>
  { #each socialLinks as { href, src, alt } }
    <a class='social-link' {href} target='_blank' >
      <img class='social-icon'{src} {alt} />
    </a>
  { /each }
</div>

<style>
  .social-link {
    text-decoration: none;
  }

  .social-icon {
    height: 31px;
    width: 31px;
    border-radius: 16px;
    border: 1px solid transparent;
    margin-right: 12px;
  }

  .social-icon:hover {
    border: 1px solid var(--medium-grey1);
  }
  
  .on-dark .social-icon:hover {
    border: 1px solid var(--light-grey);
  }
</style>