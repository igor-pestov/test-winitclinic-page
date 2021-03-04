<template>
  <div>
    <HealthPros class="desktop" />

    <HealthProsMobile class="mobile" />
  </div>
</template>
<script>
import HealthPros from "../components/HealthPros/index.vue";
import HealthProsMobile from "../components/HealthProsMobile/index.vue";
export default {
  components: {
    HealthPros,
    HealthProsMobile,
  },
};
</script>

<style lang="scss">
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