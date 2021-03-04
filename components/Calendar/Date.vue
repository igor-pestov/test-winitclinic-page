<template>
    <div class="date">
      <div class="day">
        <img
          class="back"
          src="@/assets/images/icon-chevron-right.svg"
          alt="error"
        />
        1 — 7 November
        <img
          class="next"
          src="@/assets/images/icon-chevron-right.svg"
          alt="error"
        />
      </div>
      <div class="week">
        <div
          class="day_of_week"
          v-bind:class="{
            active: day.isActive,
            disabled: day.isDisabled,
          }"
          v-for="(day, i) in week"
          :key="i"
          v-bind:index="i"
        >
          <span>{{ day.name }}</span>
          <div class="block">
            {{ i + 1 }}
          </div>
        </div>
      </div>
      <div class="hour">
        <div
          class="minute"
          v-for="(minute, i) in hour"
          :key="i"
          v-bind:class="{
            active: minute.isActive,
          }"
        >
          {{ minute.name }}
        </div>
      </div>
    </div>
</template>

<script>
export default {
  props: {
    week: {
      type: Array,
      requred: true,
    },
    hour: {
      type: Array,
      requred: true,
    },
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300&display=swap");

.date {
    .day {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-family: Lato;
      font-size: 16px;
      letter-spacing: 0.2px;
      line-height: 22px;

      .back {
        transform: rotate(180deg);
      }
    }

    .week {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 30px;
      .day_of_week {
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

        .block {
          height: 33px;
          width: 46px;
          border: 2px solid rgba(122, 39, 197, 1);
          border-left: 1px solid rgba(122, 39, 197, 1);
          border-right: 1px solid rgba(122, 39, 197, 1);
          color: rgba(122, 39, 197, 1);
          font-family: Lato;
          font-size: 12px;
          display: flex;
          justify-content: center;
          align-items: center;
          cursor: pointer;
          transition: 1s;

          @media (max-width: 1024px) {
            width: 43px;
          }

          &:hover {
            background-color: rgba(122, 39, 197, 1);
            color: #fff;
          }
        }
      }

      .active {
        .block {
          background-color: rgba(122, 39, 197, 1);
          color: #fff;
        }
      }

      .disabled {
        .block {
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

    .hour {
      display: flex;
      margin-top: 30px;
      box-shadow: 0 4px 10px 0 rgba(0, 0, 0, 0.05);

      .active {
        background-color: rgba(122, 39, 197, 1);
        color: #fff;
      }

      .minute {
        height: 32px;
        width: 79px;
        font-family: Lato;
        font-size: 12px;
        border-right: 1px solid rgba(230, 230, 230, 1);
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        transition: 1s;

        &:hover {
          background-color: rgba(122, 39, 197, 1);
          color: #fff;
        }

        &:last-child {
          border: none;
        }
      }
    }
  }
</style>