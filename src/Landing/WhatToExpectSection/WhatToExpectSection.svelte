<script>
  import Section from '../../sharedComponents/Section.svelte'
  import Card from '../../sharedComponents/Card.svelte'

</script>

<Section narrow>
  <h3>What should you expect in the coming days?</h3>

  <div class='card-container'>
    <Card title='August 10'>
      <p>Frequently Asked Questions</p>
    </Card>
    <Card title='August 14'>
      <p>Declaration and defense of demands</p>
    </Card>
    <Card title='August 18' peach>
      <p>Union resource guide and action plan</p>
      <p>Mutual aid resource guide and action plan</p>
      <p>Public outreach guide</p>
      <p>Complete action plan for the October Resistance</p>
      <p>Statewide canvassing and event planning</p>
    </Card>
  </div>
</Section>

<style>
  h3 {
    color: var(--black);
    margin-bottom: 50px;
  }

  .card-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin: -16px;
  }
</style>