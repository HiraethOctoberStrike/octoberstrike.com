<script>
  import OrganizationListContainer from './OrganizationListContainer/OrganizationListContainer.svelte'
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section>
  <h3>Local Mutual Aid Organizations</h3>
  <OrganizationListContainer />

</Section>

<style>
  h3 {
    color: var(--black);
    margin-bottom: 50px;
  }
</style>

  