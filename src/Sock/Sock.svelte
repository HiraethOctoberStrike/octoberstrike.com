<script>
  import Button from '../sharedComponents/Button.svelte';
  export let navy = false;
  export let red = false;
  export let joinTheMovement = false;
</script>

<section class='sock' class:navy class:red>
  <h3>
    Stay connected and up to date on The Movement, subscribe to our email list
    here.
  </h3>
  <div id='mc_embed_signup'>
    <form
      id='mc-embedded-subscribe-form'
      name='mc-embedded-subscribe-form'
      action='https://gmail.us5.list-manage.com/subscribe/post?u=bfe81c7a2b6d480fa4a3e36dc&amp;id=6919a5c507'
      method='post'
      target='_blank'
      novalidate
    >
      <div id='mc_embed_signup_scroll'>
        <div class='subscribe-form-email-container'>
          <input
            type='email'
            name='EMAIL'
            class='subscribe-form-email'
            id='mce-EMAIL'
            placeholder='johnnyappleseed@mail.com'
            required
          />
          <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
          <div style='position: absolute; left: -5000px;' aria-hidden='true'>
            <input
              type='text'
              name='b_bfe81c7a2b6d480fa4a3e36dc_6919a5c507'
              tabindex='-1'
              value=''
            />
          </div>
          <button
            id='mc-embedded-subscribe'
            type='submit'
            class='subscribe-form-submit peach'
          >
            <span class='button-text'>SUBSCRIBE</span>
            <span class='iconify' data-icon='mdi-arrow-right' />
          </button>
        </div>
      </div>
    </form>
  </div>

  <h4>
    Get involved now to fight for your right to a livable life in your country.
  </h4>
  <div class='buttons'>
    <Button
      text='SIGN THE PETITION'
      href='http://chng.it/kNQvH8GXL5'
      white
      external
      peach
    />
    {#if joinTheMovement}
      <Button text='JOIN THE MOVEMENT' href='/join-the-movement' />
    {/if}
  </div>
</section>

<style>
  .sock {
    padding: 60px 200px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    background-color: var(--blue);
  }

  .navy {
    background-color: var(--navy);
  }

  .peach {
    background-color: var(--peach);
    color: var(--white);
  }

  .peach:hover {
    background-color: var(--dark-peach);
  }

  .red {
    background-color: var(--red);
  }

  .subscribe-form-email-container {
    display: flex;
    justify-content: space-between;
    background-color: white;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.25);
    border-radius: 100px;
    width: 500px;
  }

  .subscribe-form-email {
    margin: 16px 16px 16px 28px;
    background: none;
    border: none;
    outline: none;
    flex: 1;
  }

  .subscribe-form-email::placeholder {
    font-style: italic;
  }

  .subscribe-form-submit {
    padding: 0 40px;
    border: 3px solid white;
    border-radius: 100px;
    cursor: pointer;
  }

  .iconify {
    display: none;
    height: 24px;
    width: 24px;
  }

  h4 {
    color: white;
    margin-top: 56px;
  }

  .buttons {
    display: flex;
    flex-direction: row;
    width: 100%;
    margin-top: 28px;
  }

  @media (max-width: 900px) {
    .sock {
      padding: 60px 80px;
    }
  }

  @media (max-width: 700px) {
    .buttons {
      flex-direction: column;
      width: unset;
      justify-content: space-between;
      height: 110px;
    }

    .sock {
      padding: 60px 40px;
    }

    .subscribe-form-email-container {
      width: max(275px, 100vw - 100px);
    }

    .subscribe-form-email {
      margin: 16px;
    }

    .subscribe-form-submit {
      padding: 0 16px;
      width: 64px;
    }

    .iconify {
      display: block;
    }

    .button-text {
      display: none;
    }
  }
</style>
