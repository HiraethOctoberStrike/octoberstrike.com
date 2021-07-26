<script>
  export let text
  export let url
  export let secondary = false
  export let tertiary = false
  export let small = false

</script>
<a 
  class:secondary
  class:tertiary
  class:small
  href={url} >
  <span class='button-text'>{text}</span>
  <span class="iconify" data-icon="mdi-arrow-right"></span>
</a>

<style>
  a {
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;
    align-self: flex-start;
    font-size: 24px;
    height: 72px;
    width: 312px;
    border-radius: 40px;
    font-weight: 500;
    color: var(--white);
    background-color: var(--black);
    text-decoration: none;
    transition: 0.1s ease-in;
  }

  .button-text {
    margin-right: 12px;
  }

  a.small {
    font-size: 16px;
    height: 46px;
    width: 282px;
    border-radius: 26px;
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
  }
</style>
