<script>
  export let text
  export let href
  export let white = false
  export let red = false
  export let peach = false
  export let large = false
  export let smallText = false
  export let navyText = false
  export let external = false

</script>
<a 
  class:white
  class:red
  class:peach
  class:large
  class:navy-text={navyText}
  class:small-text={smallText}
  target={external ? '_blank' : ''}
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
    align-self: flex-start;
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
    padding: 14px 0px 14px;
  }

  .button-text {
    margin-right: 16px;
  }

  .large .button-content {
    font-size: 28px;
  }

  .white {
    background-color: var(--white);
    color: var(--red);
  }

  .red {
    background-color: var(--red);
    color: var(--white);
  }
  
  .peach {
    background-color: var(--peach);
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

  .white:hover {
    background-color: var(--lightest-grey);
  }
  
  .white:active {
    background-color: var(--light-grey);
  }
 
  .red:hover {
    background-color: var(--dark-red);
  }
  
  .red:active {
    background-color: var(--red);
  }
 
  .peach:hover {
    background-color: var(--dark-peach);
  }
  
  .peach:active {
    background-color: var(--peach);
  }

  .iconify {
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
