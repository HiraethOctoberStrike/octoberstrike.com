<script>
  import { demands } from '../../copy.js'
</script>

<header>
  <div class='header-container'>
    <h1>National General Strike</h1>
  </div>
  <div class='demands'>
    {#each demands as { title } }
      <div class='demand'>
        <span class="iconify" data-icon="mdi-check-circle"></span>
        <h5 class='demand-text'>{title}</h5>
      </div>
    {/each}
  </div>
  <div class='background-image'>
  </div>
</header>

<style>
  header {
    position: relative;
    background-color: var(--red);
    overflow: auto;
  }

  .header-container {
    position: relative;
    z-index: 1;
    margin: 48px 128px 0px;
    background-color: var(--white);
    padding: 30px 30px 14px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
    display: inline-block;
  }

  .demands {
    position: relative;
    display: flex;
    flex-direction: column;
    color: var(--white);
    padding: 56px 50px 56px 172px;
    z-index: 1;
    width: 50%;
    box-sizing: border-box;
  }

  .demand {
    display: flex;
    flex-direction: row;
    align-items: center;
    font-size: 28px;
    margin-bottom: 32px;
  }

  .iconify {
    flex-shrink: 0;
  }

  h5 {
    margin: 0 0 0 15px;
  }

  .background-image {
    width: 50%;
    height: 100%;
    position: absolute;
    right: 0;
    top: 0;

    background-image: url('https://images.fineartamerica.com/images-medium-large/shelter-dog-square-dog-photography.jpg');
    background-position: right;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }

  @media (max-width: 1100px) {
		.demands {
      width: 100%;
    }

    .background-image {
      display: none;
    }
	}

  @media (max-width: 900px) {
    .header-container {
      margin: 48px 40px 0px;
    }

    .demands {
      padding: 56px 80px 30px;
    }
  }

  @media (max-width: 700px) {
    .header-container {
      margin: 48px 20px 0px;
    }

    .demands {
      padding: 56px 40px 30px;
    }
  }

</style>