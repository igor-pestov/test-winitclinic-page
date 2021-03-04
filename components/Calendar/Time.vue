<template>
  <div class="time">
    <div class="morning">
      <span>Morning</span>
      <div
        class="hours"
        v-for="(hours, i) in timeMorning"
        v-bind:class="{ disabled: hours.isDisabled }"
        :key="i"
      >
        {{ hours.name }}
      </div>
    </div>
    <div class="afternoon">
      <span>Afternoon</span>
      <div>
        <div
          class="hours"
          v-for="(hours, i) in timeAfternoon"
          v-bind:class="{ disabled: hours.isDisabled }"
          :key="i"
        >
          {{ hours.name }}
        </div>
      </div>
    </div>
    <div class="evening">
      <span>Evening</span>
      <div
        class="hours"
        v-for="(hours, i) in timeEvening"
        v-bind:class="{ disabled: hours.isDisabled }"
        :key="i"
      >
        {{ hours.name }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    timeMorning: {
      type: Array,
      requred: true,
    },
    timeAfternoon: {
      type: Array,
      requred: true,
    },
    timeEvening: {
      type: Array,
      requred: true,
    },
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300&display=swap");

.time {
  display: flex;
  width: 100%;
  justify-content: space-between;
  margin-top: 34px;

  .afternoon {
    width: 146px;
    justify-content: center;

    div {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      height: 185px;
    }

    span {
      width: 100%;
    }
  }

  .morning,
  .afternoon,
  .evening {
    display: flex;
    flex-direction: column;
    height: 185px;

    span {
      height: 20px;
      font-family: Lato;
      font-size: 10px;
      font-weight: bold;
      letter-spacing: 0.13px;
      line-height: 12px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .hours {
      height: 33px;
      width: 73px;
      border: 1px solid rgba(122, 39, 197, 1);
      border-top: 0.5px solid rgba(122, 39, 197, 1);
      border-bottom: 0.5px solid rgba(122, 39, 197, 1);
      color: rgba(122, 39, 197, 1);
      font-family: Lato;
      font-size: 12px;
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      transition: 1s;

      &:hover {
        background-color: rgba(122, 39, 197, 1);
        color: #fff;
      }
    }

    .disabled {
      color: rgba(194, 194, 194, 1);
      border: 1px solid rgba(230, 230, 230, 1);
      background-color: rgba(247, 247, 247, 1);
      cursor: not-allowed;

      &:hover {
        color: rgba(194, 194, 194, 1);
        border: 1px solid rgba(230, 230, 230, 1);
        background-color: rgba(247, 247, 247, 1);
      }
    }
  }
}
</style>