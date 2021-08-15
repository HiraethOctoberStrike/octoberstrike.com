<script>
  import Button from '../../../sharedComponents/Button.svelte'

  export let demand
  const { numeral, title, href, subtitles, snippet } = demand
</script>

<div class='demand-card'>
  <div class='numeral-circle'>
    <p class='numeral-text'>{numeral}</p>
  </div>
  <div class='card-content'>
    <h4>{title}</h4>
    <div class='card-content'>
      <div>
        {#each subtitles as subtitle}
          <h6>{@html subtitle}</h6>
        {/each}
        <p>{@html snippet}</p>
      </div>
    </div>
  </div>
  <div class='button-container'>
    <Button text='LEARN MORE' href={href} white />
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
    background-color: var(--navy);
  }

  .numeral-text {
    color: var(--blue);
    font-family: 'Brix-Slab';
    font-weight: 900;
    font-size: 30px;
  }

  h4 {
    color: var(--black);
  }
  
  h6 {
    margin: 40px 0 20px;
  }

  .card-content {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
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
</style>