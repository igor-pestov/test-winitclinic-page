<template>
  <div class="information">
    <h1>{{ data.heading }}</h1>
    <p>
      {{ data.text }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
      requred: true,
    },
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300&display=swap");
.information {
  width: 100%;
  margin-top: 52px;

  h1 {
    font-size: 24px;
    font-weight: bold;
    font-family: Quicksand;
  }

  p {
    width: 70%;
    margin-top: 18px;
    color: #333333;
    font-family: Lato;
    font-size: 16px;
    letter-spacing: 0.2px;
    line-height: 22px;

    @media (max-width: 1024px) {
      width: 100%;
    }
  }
}
</style>