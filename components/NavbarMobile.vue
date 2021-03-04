<template>
<div>
  <div class="navbarMobile">
    
    <div class="navbarMobile__left">
      <img src="../assets/images/logo.png" alt="" />
    </div>
    <div class="navbarMobile__right">
      <img src="../assets/images/shop.svg" alt="" />
      <img  src="../assets/images/burger.svg" alt=""  />
    </div>
    
  </div>
  </div>
</template>
<script>
 
export default {
   
};
</script>

<style lang="scss">
.menu{
    position: fixed;
    width: 100%;
    height: 100vh;
    background-color: white;
    display: none;
    z-index: 100;
  }
  .open{
   
    
    display: block !important;
    position: fixed;
    top: 9%;
    width: 100%;
    height: 100vh;
    background-color: white;
    z-index: 100;
  
  }
.navbarMobile {
  
    position: fixed;
    top: 0;
    z-index: 10;
  display: flex;
  justify-content: space-between;
  padding: 15px;
  width: 100%;
  background-color: white;
  box-shadow:0 4px 10px 0 rgba(0,0,0,0.05);
  .navbarMobile__left {
    img {
      width: 120px;
    }
  }
  .navbarMobile__right {
    margin-top: 5px;
    img:first-child{
        
        margin-right: 20px;
    }
    
  }
  
  
}
</style>