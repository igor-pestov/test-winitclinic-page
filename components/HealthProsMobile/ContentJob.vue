<template>
  <div class="healthProsMobile__job">
    <img src="@/assets/images/ds-message-right-bg.svg" alt="" />
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
.healthProsMobile__job {
      margin: 30px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: relative;
      background-color: white;
      box-shadow: 0 4px 10px 0 rgba(0, 0, 0, 0.05);
      width: 90%;
      margin: 0 auto;
      height: 300px;
      margin-bottom: 15px;
      img {
        z-index: 1;
        height: 100%;
        position: absolute;
        right: 0;
      }
      .text {
        text-align: center;
        z-index: 2;
        position: relative;
        font-weight: bold;
        font-size: 30px;
        margin-bottom: 15px;
        p:last-child {
          font-size: 16px;
        }
      }
    }
</style>