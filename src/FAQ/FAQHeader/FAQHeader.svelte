<script>
  </script>
  
  <header>
    <div class='header-container'>
      <h1>Frequently Asked Questions</h1>
    </div>
    <div class='background-image'></div>
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
      padding: 30px;
      margin-bottom: 200px;
      box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
      display: inline-block;
    }
  
    .background-image {
      width: 100%;
      height: 100%;
      position: absolute;
      right: 0;
      top: 0;
  
      background-color: var(--white);
      background-image: url('/assets/images/pexels-rosemary-ketchum-1464224.jpeg');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
    }
  
    @media (max-width: 1100px) {
  
      .background-image {
        display: none;
      }
    }
  
    @media (max-width: 900px) {
      .header-container {
        margin: 48px 40px 0px;
      }
    }
  
    @media (max-width: 700px) {
      .header-container {
        margin: 48px 20px 0px;
      }
    }
  
  </style>