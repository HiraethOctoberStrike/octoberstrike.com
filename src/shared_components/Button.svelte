<script>
  export let text
  export let disabled = false
  export let url

</script>

<a 
  class:disabled 
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
    font-weight: 500;
    height: 72px;
    padding: 0 48px;
    border-radius: 40px;
    color: var(--white);
    background-color: var(--black);
    transition: 0.1s ease-in;
  }

  .button-text {
    margin-right: 12px;
  }

  a:hover {
    background-color: var(--dark-grey);
    text-decoration: none;
  }

  a.disabled {
    opacity: 0.3;
  }

  a:not(:disabled):active {
    background-color: var(--medium-grey1);
  }


</style>
