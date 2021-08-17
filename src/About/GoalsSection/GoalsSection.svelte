<script>
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section narrower>
  <h3>Our goals</h3>
  <div class='goals'>
    <h6>
      Passage of legislation surrounding our <a href='/home'>X demands</a> by October 14th, to be enacted January 1st, 2022. 
    </h6>
    <h6>
      Raising $20 billion for mutual aid funds by October 14th, from the wealthiest Americans who have long benefited off of our labor.
    </h6>
  </div>
</Section>

<style>
  h3 {
    color: var(--black);
  }
  
  .goals {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    box-sizing: border-box;
    margin: -12px;
  }

  h6 {
    flex: 1 1 20%;
    border: 1px solid var(--navy);
    padding: 40px;
    margin: 12px;
    border-radius: 12px;
  }

  @media (max-width: 900px) {
	  h6 {
      flex: 1 1 100%;
    }
  }
</style>