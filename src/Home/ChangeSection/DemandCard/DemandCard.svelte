<script>
  import Button from '../../../sharedComponents/Button.svelte'

  export let demand

  const { numeral, title, description, essayLink } = demand
</script>

<div class='demand-card'>
  <div class='numeral-circle'>
    <p class='numeral-text'>{numeral}</p>
  </div>
  <div class='card-content'>
    <h4>{title}</h4>
    <div class='description'>
      {#each description as subdemand}
        <p class='subdemand'>{subdemand}</p>
      {/each}
    </div>
  </div>
  <div class='button-container'>
    <Button text='LEARN MORE' href={essayLink} external white />
  </div>
</div>

<style>
  .demand-card {
    position: relative;
    display: flex;
    box-sizing: border-box;
    flex: 1 1 40%;
    background-color: var(--white);
    margin: 25px;
    padding: 45px;
    border: 1px solid var(--navy);
    border-radius: 12px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .numeral-circle {
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 70px;
    height: 70px;
    top: -35px;
    left: -35px;
    border-radius: 100px;
    background-color: var(--blue);
  }

  .numeral-text {
    color: var(--navy);
    font-family: 'Brix-Slab';
    font-weight: 900;
    font-size: 30px;
  }

  h4 {
    color: var(--black);
  }
  
  .subdemand {
    margin-top: 10px;
  }

  .card-content {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .description {
    margin-top: 20px;
  }

  .button-container {
    align-self: flex-start;
    justify-self: flex-end;
    margin: 10px 0 -14px -30px;
  }

  @media (max-width: 1100px) {
    .demand-card {
      flex: 1 1 100%;
    }
  }
 
  @media (max-width: 500px) {
    .button-container {
      margin: 10px 0 -14px -16px;
    }
  }
</style>