<script>
  // TODO: REMOVE IF STILL UNUSED
  
  import Button from './Button.svelte'

  export let header;
  export let paragraph;
  export let buttonText;
  export let buttonHref;
  export let smallText = false;
</script>

<section class='header-w-cta'>
  <h4>October 15 2021</h4>
  <h1>{header}</h1>
  <p>{paragraph}</p>
  <Button text={buttonText} href={buttonHref} {smallText} />
</section>

<style>
  .header-w-cta {
    display: flex;
    flex-direction: column;
    padding-top: 134px;
    padding-bottom: 100px;
    background-color: var(--light-grey);
  }

  h4 {
    margin-bottom: 24px;
  }

  h1 {
    margin-bottom: 24px;
  }

  p {
    max-width: 550px;
    margin-bottom: 42px;
  }

  @media (max-width: 500px) {
    .header-w-cta {
      padding-top: 100px;
      padding-bottom: 80px;
    }
  }
</style>