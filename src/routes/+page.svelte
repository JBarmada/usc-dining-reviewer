<script>
    import LandingPage from "../lib/components/LandingPage.svelte";
</script>

<div class="container">
    <div class="titleBar">
        <div class="logo">
            <img src="assets/myDiningReview.png" alt="Website Logo" />
        </div>
        <div class="user-info">
            <img src="assets/defaultpfp.png" alt="User Icon" class="user-icon" />
            <span class="dropdown-arrow">▼</span>
        </div>
    </div>
    <div class="inner-container">
        <LandingPage/>
    </div>
</div>

<style>
    .container {
        background-color: #ccc;
    }

    .titleBar {
        background-color: white;
        padding: 0.5rem;
        display: flex;
        align-items: center;
        width: 100%;
        height: 10vh;
        box-sizing: border-box;
    }
  
    .logo {
        flex-grow: 1; 
        display: flex; 
        justify-content: center;
        height: 30px;
    }
  
    .user-info {
        display: flex;
        align-items: center;
        color: white;
    }
  
    .user-icon {
        height: 2rem;
    }
  
    .dropdown-arrow {
        margin-left: 0.5rem;
        color: black;
    }
  </style>