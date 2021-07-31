<script>
  export let text
  export let href
  export let secondary = false
  export let tertiary = false
  export let large = false
  export let smallText = false
  export let navyText = false

</script>
<a 
  class:secondary
  class:tertiary
  class:large
  class:navy-text={navyText}
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
    align-self: start;
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
    padding: 14px 0px 10px;
  }

  .button-text {
    margin-right: 16px;
  }

  .large .button-content {
    font-size: 28px;
  }

  .secondary {
    background-color: var(--white);
    color: var(--red);
  }

  .tertiary {
    background-color: var(--red);
    color: var(--white);
  }

  .navy-text {
    color: var(--navy);
  }

  a:hover {
    background-color: var(--dark-grey);
  }

  a:active {
    background-color: var(--medium-grey1);
  }

  .secondary:hover {
    background-color: var(--light-grey);
  }
  
  .secondary:active {
    background-color: var(--lightest-grey);
  }

  .iconify {
    top: -2px;
    position: relative;
    flex-shrink: 0;
    height: 24px;
    width: 24px;
  }

  @media (max-width: 500px) {
    .button-content {
      font-size: 14px;
      margin: 0 16px;
    }

    a.small-text .button-text {
      font-size: 13px;  
    }
    
    .large .button-content {
      font-size: 18px;
    }
  }
</style>
