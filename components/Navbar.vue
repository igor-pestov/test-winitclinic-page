<template>
  <div class="navbar">
    <!-- <img src="../assets/images/favicon.png" alt=""> -->
    <div class="navbar__container">
      <img
        class="navbar__container_logo"
        src="../assets/images/logo.png"
        alt=""
      />
      <div class="navbar__container_popup">
        <p>Our health tests</p>
        <img src="../assets/images/select-arrow-icon.svg" alt="" />
      </div>
      
      <nuxt-link to="/healthPros" class="navbar__container_item">Health Pros</nuxt-link>
      <div class="navbar__container_item">Register Kit</div>
      <div class="navbar__container_item">About us</div>
      <div class="navbar__container_phone">
          
          <img src="../assets/images/icon-phone.svg" alt="">
            <p>8 800 1234 567</p>
          </div>
      <div class="navbar__container_signin">Sign in</div>
      <div class="navbar__container_cart">
          <img src="../assets/images/cart.svg" alt="">
          <p>Cart</p>
          </div>
    </div>
  </div>
</template>

<script></script>

<style lang='scss'>
.navbar {
  background-color: white;
box-shadow: 0 4px 10px 0 rgba(0,0,0,0.05);
  .navbar__container {
    font-weight: bold;
     max-width: 1200px;
    margin: 0 auto;
    padding: 10px 0px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .navbar__container_logo {
      width: 150px;
    }
    .navbar__container_popup {
      display: flex;
      p {
        margin-right: 10px;
      }
      img {
        margin-top: 5px;
        cursor: pointer;
      }
    }
    .navbar__container_phone {
        display: flex;
      color: #7a25cb;
      border: 1px solid #7a25cb;
      padding: 15px 20px;
      border-radius: 30px;
      cursor: pointer;
        img{
            margin-right: 10px;
        }
    }
    .navbar__container_cart {
      
        display: flex;
        align-items: center;
      color: #7a25cb;
        img{
            margin: 0px 10px 10px 0px;
        }
    }
    .navbar__container_item{
      cursor: pointer;
    }
    .navbar__container_signin{
      cursor: pointer;

    }
  }
}
</style>