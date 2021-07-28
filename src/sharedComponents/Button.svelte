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
    height: 72px;
    min-width: 312px;
    max-width: 350px;
    border-radius: 40px;
    font-weight: 500;
    color: var(--white);
    background-color: var(--black);
    text-decoration: none;
    transition: 0.1s ease-in;
    margin-right: 30px;
  }

  .button-content {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    margin: 0 30px;
    font-size: 24px;
  }

  .button-text {
    margin-right: 12px;
  }

  a.small {
    height: 46px;
    width: 282px;
    border-radius: 26px;
  }
  
  a.small .button-content {
    font-size: 16px;
  }

  a.small-text .button-text {
    font-size: 18px;  
  }

  a.secondary {
    background-color: var(--red);
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
    top: -1px;
    position: relative;
    flex-shrink: 0;
  }

  @media (max-width: 700px) {
    a {
      height: 60px;
      min-width: 250px;
    }

    .button-content {
      font-size: 18px;
    }

    a.small-text .button-text {
      font-size: 13px;  
    }
  }
</style>
