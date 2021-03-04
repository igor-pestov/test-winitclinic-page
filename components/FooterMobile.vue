<template>
  <div class="footerMobile">
    <div class="footerMobile__row-1">
      <img src="../assets/images/icon-phone.svg" alt="" />
      <p>8 800 1234 567</p>
    </div>
    <div class="footerMobile__row-2">
      <p>About us</p>
      <i></i>
      <p>Our Tests</p>
      <i></i>
      <p>Register Kit</p>
      <p>Privacy Policy</p>
      <i></i>
      <p>Terms of Service</p>
    </div>
    <div class="footerMobile__row-3">
      <img class="stores" src="@/assets/images/footer/google-play.png" alt="" />
      <img class="stores" src="@/assets/images/footer/app-store.png" alt="" />
    </div>
    <div class="footerMobile__row-4">
      <div class="social">
        <img class="stores" src="@/assets/images/icon-fb.svg" alt="" />
        <img class="stores" src="@/assets/images/icon-fb.svg" alt="" />
        <img class="stores" src="@/assets/images/icon-fb.svg" alt="" />
      </div>
      <div class="copy">
        <h4>2020 © WINIT</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.footerMobile {
  background-color: #0d0044;
  width: 100%;
  color: white;
  .footerMobile__row-1 {
    display: flex;
    color: #bdbdbd;
    border: 1px solid #bdbdbd;
    width: 80%;

    margin: 30px auto;
    padding: 10px 0px;
    border-radius: 30px;
    justify-content: center;
    cursor: pointer;
    img {
      margin-right: 10px;
      color: #bbbbbb;
    }
  }
  .footerMobile__row-2 {
    display: flex;
    width: 60%;
    flex-wrap: wrap;
    text-align: center;
    margin: 0 auto;
    font-size: 13px;
    align-items: center;
    justify-content: center;
    margin-bottom: 30px;

    i {
      width: 5px;
      height: 5px;
      border-radius: 10px;
      background-color: #bbbbbb;
      margin: 0 8px;
    }
  }
  .footerMobile__row-3 {
    display: flex;
    justify-content: space-around;
    margin-bottom: 30px;

    img {
      width: 170px;
      height: 60px;
    }
  }
  .footerMobile__row-4 {
    display: flex;
    justify-content: space-around;
    margin-bottom: 30px;
    img {
      margin-right: 10px;
    }
    h4 {
      color: #bbbbbb;
    }
  }
}
</style>