<script>
  import Button from '../sharedComponents/Button.svelte'
  import Section3 from './Section3/Section3.svelte'

</script>

<section class='section-1'>
  <h4>October 15 2021</h4>
  <h1>National General Strike</h1>
  <p>
    Lorem ipsume dolor sit amet, consectetur adipiscing elit. Ornare duis lacus neque adipiscing aliquam molestie fermentum. Eget commodo quisque non, porta. In congue sociis donec vel laoreet in pharetra. Vitae habitant et.
  </p>
  <Button text='STRIKE WITH US' href='/strike-with-us' />
</section>

<Section3 />


<style>

  section {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  .section-1 {
    padding: 134px 165px 104px;
    background-color: var(--light-grey);
  }


</style>