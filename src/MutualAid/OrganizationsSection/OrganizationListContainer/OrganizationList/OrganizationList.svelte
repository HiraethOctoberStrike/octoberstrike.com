<script>
  import Button from '../../../../sharedComponents/Button.svelte'
  
  export let aidOrgs
</script>

{#if aidOrgs}
  {#each aidOrgs as { state, abbreviation, name, href } }
    <div class='organization'>
      <h6>{name}</h6>
      <div class='org-right'>
        <p class='abbreviation'>{abbreviation}</p>
        <div class='button-container'>
          <Button text='LEARN MORE' {href} secondary />
        </div>
      </div>
    </div>
  {/each}
{/if}


<style>
  .organization {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 16px;
    border: 1px solid var(--black);
  }

  .organization:nth-child(odd) {
    border: 1px solid var(--navy);
  }

  .org-right {
    display: flex;
    flex-direction: row;
    align-items: center;    
    margin-left: 16px;
  }

  h6 {
    background-color: var(--black);
    padding: 16px 30px 12px;
    max-width: 220px;
    color: var(--white);
    flex: 1;
  }

  .organization:nth-child(odd) h6 {
    background-color: var(--navy);
  }

  .abbreviation {
    color: var(--black);
    margin: 0 40px 0 20px;
  }

  .button-container {
    margin: 0 -10px 0 46px;
  }


  @media (max-width: 1100px) {
    h6 {
      padding: 16px 16px 12px;
    }

    .abbreviation {
      margin: 0px 20px;
    }

    .button-container {
      margin-left: unset;
    }
  }

  @media (max-width: 700px) {
    .abbreviation {
      font-size: 12px;
      line-height: 16px;
    }
  }

  @media (max-width: 500px) {
    .button-container {
      width: 130px;
    }

    .abbreviation {
      margin: 5px 0;
    }
  }
</style>