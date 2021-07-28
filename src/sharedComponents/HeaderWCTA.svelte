<script>
  import Button from './Button.svelte'

  export let header;
  export let paragraph;
  export let buttonText;
  export let buttonHref;
  export let smallText = false;
</script>

<section class='section-1'>
  <h4>October 15 2021</h4>
  <h1>{header}</h1>
  <p>{paragraph}</p>
  <Button text={buttonText} href={buttonHref} {smallText} />
</section>

<style>
  .section-1 {
    display: flex;
    flex-direction: column;
    padding: 134px 165px 104px;
    background-color: var(--light-grey);
  }

  .section-1 p {
    max-width: 550px;
  }
  @media (max-width: 900px) {
    .section-1 {
      padding: 134px 80px 104px;
    }
  }
  
  @media (max-width: 700px) {
    .section-1 {
      padding: 134px 40px 104px;
    }
  }

  @media (max-width: 500px) {
    .section-1 {
      padding: 100px 20px 80px;
    }
  }
</style>