<template>
  <div class="healthProsMobile__help">
    <img src="@/assets/images/ds-message-right-bg.svg" alt="" />
    <div class="text">
      <p>Need help?</p>
      <p>Get yor free health consultation today</p>
    </div>
        <Button v-bind:name="'Post a job'" v-bind:color="'success'" />

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
.healthProsMobile__help {
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
        margin-bottom: 65px;
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