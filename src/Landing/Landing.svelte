<script>
  import Button from '../sharedComponents/Button.svelte'
</script>

<section class='landing-page'>
  <div class='h1-container'>
    <h1>We’re glad you’re here</h1>
  </div>
  <img src='/assets/images/LMX_Logo_White-8.png' alt='labor movement x logo' />
  <h5>We are at the start of something great.</h5>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam aliquam, ex at elementum congue, lacus lectus facilisis sapien, non eleifend justo ligula ut quam. Aenean turpis massa, imperdiet sit amet dignissim vitae, venenatis pretium urna. Morbi id velit quis nunc dictum tincidunt. Suspendisse ultricies turpis eu volutpat elementum. Nunc tristique nulla at elit dictum, ut tincidunt ligula dignissim. Etiam mollis nibh nisi, vitae elementum turpis vestibulum quis. Morbi ut lacus et velit sollicitudin facilisis. Maecenas eu sodales elit. Vivamus laoreet lectus id nisi tristique, quis condimentum est fermentum.
  </p>
  <p>
    Nam sodales odio vitae ornare efficitur. Donec malesuada posuere tortor, nec viverra est facilisis quis. Nulla id lacus maximus, finibus lacus eget, venenatis quam. Ut laoreet ante ac condimentum faucibus. Nunc id quam vehicula, placerat orci eget, mollis lectus. Maecenas sit amet vehicula purus. In pellentesque porttitor dolor, sed vulputate sem euismod vel. Morbi eu ullamcorper nulla. Nunc tempus ultricies nibh, eget fringilla metus posuere vitae. Etiam aliquet mattis laoreet. Donec imperdiet, sapien eget dictum consequat, ante tortor efficitur urna, eu accumsan nibh ligula a magna.
  </p>
  <p>
    Proin id lectus a nisl tempor tincidunt. Aenean nec lobortis lacus. Pellentesque vitae congue nulla. Vestibulum semper ultrices felis, eget rhoncus tortor sodales molestie. Donec tincidunt ullamcorper consectetur. Duis lectus odio, suscipit ac massa a, euismod ultrices erat. Aliquam rutrum lacini.
  </p>
  <div class='button-container'>
    <Button text='CONTINUE TO SITE' href='/home' secondary />
  </div>
</section>

<style>
  .landing-page {
    display: flex;
    flex-direction: column;
  }

  .h1-container {
    position: relative;
    background-color: var(--white);
    padding: 30px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
    display: inline-block;
  }

  .landing-page {
    background-color: var(--navy);
  }

  img {
    width: 158px;
    margin: 60px 0 12px;
  }

  h5 {
    margin-bottom: 36px;
  }

  p {
    color: var(--white);
    margin-bottom: 24px;
  }

  .button-container {
    margin-top: 24px;
    align-self: flex-start;
  }

</style>