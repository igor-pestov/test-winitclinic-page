<template>
  <div class="healthPros__content_right_job">
    <img class="left" src="@/assets/images/ds-message-left-bg.svg" alt="" />
    <img class="right" src="@/assets/images/ds-message-right-bg.svg" alt="" />
    <div class="text">
      <p>Don`t know who to select?</p>
      <p>Let us match you</p>
    </div>
    <Button v-bind:name="'Post a job'" v-bind:color="'primary'" />
  </div>
</template>

<script>
import Button from "../Button";
export default {
  components: {
    Button,
  },
};
</script>

<style lang="scss" scoped>
.healthPros__content_right_job {
  height: 200px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: relative;
  background-color: white;
  box-shadow: 0 4px 10px 0 rgba(0, 0, 0, 0.05);
  margin-bottom: 12px;
  .left {
    z-index: 1;
    height: 100%;
    position: absolute;
    left: 0;
  }
  .right {
    z-index: 1;
    height: 100%;
    position: absolute;
    right: 0;
  }
  .text {
    z-index: 2;
    position: relative;
    font-weight: bold;
    font-size: 30px;
    p:first-child {
      font-family: "Quicksand", sans-serif;
    }
    p:last-child {
      font-size: 16px;
    }
  }
}
</style>