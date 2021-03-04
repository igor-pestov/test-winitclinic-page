<template>
  <div>
    <div v-if="isCloseSelect" class="field">
      <div class="header">
        <p>{{ heading }}</p>
        <img
          v-if="close"
          @click.prevent="setClose"
          src="@/assets/images/icon-cross.svg"
          alt="error"
        />
      </div>

      <select type="text" autocomplete="off" id="em">
        <option value="" disabled selected>{{ placeholder }}</option>
      </select>
      <img class="arrow" src="@/assets/images/select-arrow-icon.svg" alt="" />
    </div>

    <div v-else>
      <hr />
      <div class="plus_field">
        <p>{{ heading }}</p>
        <img
          @click.prevent="setClose"
          src="@/assets/images/icon-cross.svg"
          alt="error"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isCloseSelect: this.isClose
    };
  },
  props: {
    heading: {
      type: String,
      requred: true,
    },
    placeholder: {
      type: String,
      requred: true,
    },
    close: {
      type: Boolean,
    },
    isClose: {
      type: Boolean,
    },
  },
  methods: {
    setClose() {
      this.isCloseSelect = !this.isCloseSelect;
    },
  },
};
</script>

<style lang="scss" scoped>
.field {
  position: relative;
  margin-bottom: 10px;
  .header {
    margin-bottom: 10px;
    display: flex;
    justify-content: space-between;
    img {
      margin-right: 10px;
      margin-top: 5px;
      cursor: pointer;
    }
  }

  select {
    height: 49px;
    width: 100%;
    border: 1px solid #cfcfcf;
    border-radius: 5px;
    background-color: white;
    color: rgba(132, 132, 132, 1);
    font-family: Lato;
    font-size: 14px;
    letter-spacing: 0;
    padding: 0 19px 0 14px;
    appearance: none;
    &:focus {
      outline: 0;
      border-color: black;
    }
  }
  .arrow {
    position: absolute;
    right: 6%;
    margin-top: 20px;
    cursor: pointer;
  }
}

hr {
  border: none;
  background-color: rgb(224, 224, 224);
  color: rgb(224, 224, 224);
  height: 1px;
  margin-bottom: 10px;
}
.plus_field {
  display: flex;
  justify-content: space-between;
  color: #7a25cb;
  margin-bottom: 10px;
  img {
    transform: rotate(-45deg);
    margin-right: 10px;
    cursor: pointer;
  }
}
</style>