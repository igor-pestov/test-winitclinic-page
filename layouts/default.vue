<template>
  <div class="container">
      <Navbar class="desktop" />
      <NavbarMobile class="mobile" />
    <main>
      <Nuxt />
    </main>
    <Footer  class="desktop"  />
    <FooterMobile class="mobile" />
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import NavbarMobile from "../components/NavbarMobile.vue";
import Footer from "../components/Footer.vue";
import FooterMobile from "../components/FooterMobile.vue";

export default {
  components: {
    Navbar,
    NavbarMobile,
    Footer,
    FooterMobile
  },
  
};
</script>

<style lang='scss'>
@import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&family=Quicksand:wght@300;400;500;600;700&display=swap');
html {
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
body {
  padding: 0;
  margin: 0;
  height: 100%;
  // font-family: 'Quicksand', sans-serif;
  font-family: 'Lato', sans-serif;
  background-color: #f3f3f3;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
a{
  text-decoration: none;
  color: black;
}

.container {
  width: 100%; /*main container*/
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  min-height: 100%;
}
@media (max-width: 1440px) {
  .desktop {
    display: none;
  }
}

@media (min-width: 1440px) {
  .mobile {
    display: none;
  }
}
</style>
