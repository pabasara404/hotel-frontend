<template>
    <div class="navbar-container">
      <div class="header">
        <div class="headerLeft">
          <img src="@/assets/logo.png" />
        </div>
        <div class="headerRight">
          <router-link to="/" class="nav-link">Home</router-link>
          <router-link to="/about" class="nav-link">About Us</router-link>
          <router-link to="/contact" class="nav-link">Contact Us</router-link>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    // You can add data properties or methods here if needed
  };
  </script>
  
  <style scoped>
  .navbar-container {
    position: sticky;
    top: 0;
    z-index: 100; /* Ensure it's above other content */
    background-color: white; /* Set a background color if needed */
  }
  
  .header {
    height: 60px;
    display: flex;
    align-items: center;
    border-bottom: 1px solid rgb(223, 221, 221);
    box-shadow: 0px 4px 4px -2px rgba(0, 0, 0, 0.178);
  }
  
.headerLeft img{
    object-fit:contain;
    width: 109px;
    height: 40px;
    margin-left: 5px;
    
}
.headerLeft{
    display: flex;
    padding-left: 10px;
    padding-right: 10px;
    
}
  
  /* Style the router-links */
  .nav-link {
    text-decoration: none;
    padding: 20px;
    font-weight: 500;
    color: #777;
  }
  
  .nav-link:hover {
    background-color: rgb(238, 238, 238);
  }
  
  .active {
    background-color: antiquewhite !important;
    color: brown !important;
  }
  </style>
  