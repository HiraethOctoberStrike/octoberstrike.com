<script>
  export let onDark = false;

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