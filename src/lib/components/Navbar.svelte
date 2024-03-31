<script>
    // Props could include the image source and any actions for the login button
    let imgSrc = "/assets/usclogo.png";
    export let onLogin = () => {};
  </script>
  
  <nav class="navbar">
    <div class="navbar-content">
      <img src={imgSrc} alt="Logo" class="logo"/>
    </div>
  </nav>
  <div class="test">

  </div>
  
  <style>
    .navbar {
      background-color: #990000;
      display: flex;
      justify-content: space-between;
      height: 10vh;
    }
  
    .navbar-content {
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 100%;
    }
  
    .logo {
      height: 10vh;
    }
  </style>