<template>
  <button class="btn" v-bind:class="[color]">{{ name }}</button>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      requred: true,
    },
    color: {
      type: String,
      requred: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.btn {
  border-radius: 24px;
  color: #fff;
  z-index: 2;
  padding: 14px 42px;
  font-family: Lato;
  font-size: 16px;
  font-weight: bold;
  border: none;
  transition: 0.5s;
  cursor: pointer;
}
.success {
  background-color: rgba(11, 183, 0, 1);
  &:hover {
    background-color: #4eda44;
  }
}

.primary {
  background-color: #7a25cb;
  &:hover {
    background-color: #9a51df;
  }
}
</style>