<script>
  import Button from '../sharedComponents/Button.svelte'
  export let navy = false;
  export let red = false;
  export let joinTheMovement = false;
</script>

<section class='sock' class:navy class:red >
  <h3>
    Get involved now to fight for your right to a livable life in your country.
  </h3>
  <div class='buttons'>
    <Button 
      text='SIGN THE PETITION' 
      href='http://chng.it/kNQvH8GXL5' 
      white external peach />
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

  .red {
    background-color: var(--red);
  }

  .buttons {
    display: flex;
    flex-direction: row;
    width: 100%;
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
  }
</style>