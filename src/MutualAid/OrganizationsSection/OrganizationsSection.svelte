<script>
  import { mutualAidOrgs } from '../../copy'
  import Button from '../../sharedComponents/Button.svelte'
</script>

<section class='organizations-section'>

  <h3>Local Mutual Aid Organizations</h3>
  <p class='organizations-text'>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Posuere consequat consequat rhoncus ac ac, morbi id. Pellentesque dolor in facilisi tincidunt et cras cras id dignissim. Suscipit orci, morbi pellentesque enim. Dictum et, eget lorem tortor. Aliquet nibh gravida et sagittis. Malesuada mauris justo a nisi nibh consectetur sed ut. Pretium sed dictum non, elit. Dignissim mus eget pretium lectus ac. </p>
  {#each mutualAidOrgs as { orgName, orgType, state, href } }
    <div class='organization'>
      <h6>{orgName}</h6>
      <div class='org-right'>
        <div class='org-info'>
          <p>{orgType}</p>
          <p>{state}</p>
        </div>
        <div class='button-container'>
          <Button text='LEARN MORE' {href} secondary />
        </div>
      </div>
    </div>
  {/each}
</section>

<style>
  h3 {
    color: var(--black);
  }
  
  .organizations-text {
    margin-bottom: 40px;
  }

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

  .org-info {
    display: flex;
    flex-direction: row;
    justify-content: center;
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

  .organization p {
    color: var(--black);
    margin: 0 20px;
  }

  .button-container {
    margin: 0 -10px 0 46px;
  }


  @media (max-width: 1100px) {
    h6 {
      padding: 16px 16px 12px;
    }

    .organization p {
      margin: 0px 10px;
    }

    .button-container {
      margin-left: unset;
    }
  }

  @media (max-width: 700px) {
    .organization p {
      font-size: 12px;
      line-height: 16px;
    }
  }
  
  @media (max-width: 500px) {
    .org-info {
      flex-direction: column-reverse;
      margin-right: 10px;
    }
    
    .button-container {
      width: 130px;
    }

    .organization p {
      margin: 5px 0;
    }
  }
</style>