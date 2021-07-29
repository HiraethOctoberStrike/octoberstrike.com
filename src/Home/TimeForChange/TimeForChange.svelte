<script>
  import { demands } from '../../copy.js'
  
</script>

<section class='time-for-change'>
  <h2>
    The U.S. government is not serving its people. Now is the time for change.
  </h2>
  <div class='demands'>
    {#each demands as { title, snippet }, i }
      <div class='demand' 
        class:red={[0, 4].includes(i)}
        class:navy={[3, 7].includes(i)}>
        <h5>{title}</h5>
        <p>{snippet}</p>
      </div>
    {/each}
  </div>
</section>

<style>
  .time-for-change {
    background-color: var(--white);
  }

  .demands {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    box-sizing: border-box;
    margin: -16px;
  }

  .demand {
    flex: 1 1 400px;
    background-color: var(--white);
    margin: 16px;
    border: 1px solid var(--black);
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
  }

  h5 {
    padding: 24px;
    background-color: var(--black);
  }

  p {
    padding: 18px 28px;
  }

  .red {
    border: 1px solid var(--red)
  }

  .red h5 {
    background-color: var(--red);
  }

  .navy {
    border: 1px solid var(--navy)
  }

  .navy h5 {
    background-color: var(--navy);
  }

  @media (max-width: 500px) {
    p {
      padding: 12px 20px;
    }
  }
  </style>