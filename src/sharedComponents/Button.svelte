<script>
  export let text
  export let href
  export let secondary = false
  export let tertiary = false
  export let small = false
  export let smallText = false

</script>
<a 
  class:secondary
  class:tertiary
  class:small
  class:small-text={smallText}
  {href} >
  <div class='button-content'>
    <span class='button-text'>{text}</span>
    <span class="iconify" data-icon="mdi-arrow-right"></span>
  </div>
</a>

<style>
  a {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 52px;
    max-width: 350px;
    color: var(--white);
    background-color: var(--black);
    text-decoration: none;
    transition: 0.1s ease-in;
    margin-right: 16px;
  }

  .button-content {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    margin: 0 30px;
    font-size: 18px;
    font-weight: 600;
  }

  .button-text {
    margin-right: 16px;
  }

  a.small {
    height: 46px;
    width: 282px;
    border-radius: 26px;
  }
  
  a.small .button-content {
    font-size: 14px;
  }

  /* a.small-text .button-text {
    font-size: 18px;  
  } */

  a.secondary {
    background-color: var(--white);
    color: var(--red);
  }

  a.tertiary {
    background-color: transparent;
    color: var(--red);
  }

  a:hover {
    background-color: var(--dark-grey);
  }

  a:active {
    background-color: var(--medium-grey1);
  }

  .iconify {
    top: -2px;
    position: relative;
    flex-shrink: 0;
    height: 24px;
    width: 24px;
  }

  @media (max-width: 500px) {
    a {
      height: 44px;
    }

    .button-content {
      font-size: 14px;
      margin: 0 16px;
    }

    a.small-text .button-text {
      font-size: 13px;  
    }
  }
</style>
