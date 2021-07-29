<script>

</script>

<section class='plan-section'>
    <img src='https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.MB8pq1-VyWEzA4NLbhy95wHaFi%26pid%3DApi&f=1' />
  <div class='plan-content'>
    <h2>We've got a plan:</h2>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ipsum, a ac est pulvinar lacus diam. Lacus, etiam massa adipiscing dui justo massa. Sapien, neque ultricies vel proin ipsum laoreet. Diam sed commodo aliquet ac ipsum pellentesque cras convallis enim. Vestibulum gravida libero eget magna arcu. Non facilisi semper augue elementum mauris quam placerat. Pulvinar scelerisque auctor orci, ultrices in. Tellus nulla metus eu proin pulvinar aliquam pulvinar odio. Eget nec porttitor velit.
    </p>
  </div>
</section>

<style>

  .plan-section {
    position: relative;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
  }

  img {
    margin-right: 50px;
    display: flex;
    flex: 0 2 50%;
    max-height: 500px;
    width: 100%;
    object-fit: contain;
  }

  .plan-content {
    display: flex;
    flex-direction: column;
    flex: 1 0 50%;
    flex-shrink: 1;
  }

  h2 {
    margin-bottom: 20px;
  }
  
  p {
    color: var(--dark-grey);
  }

  @media (max-width: 1000px) {
    .plan-section {
      flex-direction: column;
    }

    img {
      margin: 0 0 50px;
      flex: unset;
    }

    .plan-content {
      flex: unset;
    } 
  }
</style>