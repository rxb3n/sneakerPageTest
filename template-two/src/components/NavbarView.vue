<template>

    <div class="navbar">
  <!-- NAV LEFT SIDE -->

  <img class="hamburger-menu" src="@/assets/menu-btn.png" height="50" width="50">

      <div class="nav-logo">
        <img src="@/assets/logo.png" height="65" width="65">
        <p class="title">SHOE SHOP</p>
      </div>
      <!-- NAV LEFT SIDE -->
  
      <!-- NAV RIGHT SIDE -->
      <div class="nav-elements">
        <p class="active">HOME</p>
        <p>GALLERY</p>
        <p>SHOP</p>
        <p>REVIEWS</p>
        <p>CONTACT</p>
        <img src="@/assets/search-icon.png" height="25" width="25" style="padding-top: 10px;">
        <img src="@/assets/bag-icon.png" height="35" width="35" style="padding-top: 4px;"  >
      </div>
      <!-- NAV RIGHT SIDE -->
  
    </div>
  </template>
  
  <style>
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700;900&display=swap');

  
  .navbar {
    z-index: 999;
    font-weight: 700;
    background-color: white;
    top: 0;
    position: sticky;
    display: flex;
    justify-content: space-between;
    padding-left: 5%;
    padding-right: 5%;
    align-items: center;
  }

  .title {
    font-size: 1.5em;
    color: #110f42;
  }
  
  .nav-logo{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    width: 15%;
    top: 50%;
  }
  
  .nav-elements {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    width: 55%;
  }

  .active {
    color: #4843d7;
  }

  .hamburger-menu {
    display: none;
  }

  @media screen and (max-width:900px){
    .hamburger-menu {
      display: block;
    }
    .navbar-logo, .nav-elements {
      display: none;
    }
  }
  
  </style>