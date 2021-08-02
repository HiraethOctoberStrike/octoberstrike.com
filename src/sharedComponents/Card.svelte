<script>
  export let title;
  export let red = false;
  export let navy = false;
  export let small = false;
</script>

<div class='card' 
  class:red
  class:navy 
  class:small >
  <h5>{title}</h5>
  <div class='card-content'>
    <slot></slot>
  </div>
</div>

<style>
  .card {
    flex: 1 1 45%;
    background-color: var(--white);
    margin: 16px;
    border: 1px solid var(--black);
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
  }

  .card-content {
    padding: 18px 28px;
  }

  h5 {
    padding: 24px;
    background-color: var(--black);
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

  .small {
    flex: 1 1 270px;
    margin: 10px;
  }

  @media (max-width: 900px) {
    .card {
      flex: 1 1 100%;
    }
  }
</style>