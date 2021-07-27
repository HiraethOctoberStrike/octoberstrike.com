<script>
  import Button from './Button.svelte'
</script>

<section>
  <h1>
    Get involved now to fight for your right to a liveable life in your country.
  </h1>
  <div class='buttons'>
    <Button text='SIGN THE PETITION' href='http://chng.it/kNQvH8GXL5' secondary={true} />
    <Button text='GET INVOLVED' href='/get-involved' />
  </div>
</section>

<style>

  section {
    padding: 81px 179px 82px 156px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    background-color: var(--lightest-grey);
  }

  .buttons {
    display: flex;
    flex-direction: row;
    width: 100%;
  }
</style>