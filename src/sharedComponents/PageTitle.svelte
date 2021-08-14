<script>
  export let text
</script>

<div class='title-container'>
  <h1>{text}</h1>
</div>

<style>
  .title-container {
    position: relative;
    display: inline-block;
    z-index: 1;
    background-color: var(--white);
    padding: 30px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
  }

  h1 {
    overflow-wrap: break-word;
  }
</style>