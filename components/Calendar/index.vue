<template>
  <div class="сard">
    <div class="header">Book a consultation</div>
    <Date v-bind:week="week" v-bind:hour="hour" />
    <Time
      v-bind:timeMorning="timeMorning"
      v-bind:timeAfternoon="timeAfternoon"
      v-bind:timeEvening="timeEvening"
    />
    <div class="recording">
      <span>$ 90.00</span>
      <Button v-bind:name="'Book consultation'" v-bind:color="'success'" />
    </div>
  </div>
</template>

<script>
import Button from "../Button.vue";
import Date from "./Date.vue";
import Time from "./Time.vue";
export default {
  components: {
    Button,
    Date,
    Time,
  },
  data() {
    return {
      timeMorning: [
        {
          name: "9:30 am",
          isDisabled: true,
        },
        {
          name: "10:00 am",
          isDisabled: true,
        },
        {
          name: "10:30 am",
          isDisabled: false,
        },
        {
          name: "11:00 am",
          isDisabled: false,
        },
        {
          name: "11:30 am",
          isDisabled: false,
        },
      ],
      timeAfternoon: [
        {
          name: "12:00 pm",
          isDisabled: false,
        },
        {
          name: "12:30 pm",
          isDisabled: false,
        },
        {
          name: "1:00 pm",
          isDisabled: true,
        },
        {
          name: "1:30 pm",
          isDisabled: true,
        },
        {
          name: "2:00 pm",
          isDisabled: true,
        },
        {
          name: "2:30 pm",
          isDisabled: false,
        },
        {
          name: "3:00 pm",
          isDisabled: false,
        },
        {
          name: "3:30 pm",
          isDisabled: false,
        },
        {
          name: "4:00 pm",
          isDisabled: false,
        },
        {
          name: "4:30 pm",
          isDisabled: false,
        },
      ],
      timeEvening: [
        {
          name: "5:00 pm",
          isDisabled: false,
        },
        {
          name: "5:30 pm",
          isDisabled: false,
        },
        {
          name: "6:00 pm",
          isDisabled: true,
        },
        {
          name: "6:30 pm",
          isDisabled: true,
        },
        {
          name: "7:00 pm",
          isDisabled: true,
        },
      ],
      hour: [
        {
          name: "15 min",
          isActive: false,
        },
        {
          name: "30 min",
          isActive: true,
        },
        {
          name: "45 min",
          isActive: false,
        },
        {
          name: "1 hour",
          isActive: false,
        },
      ],
      week: [
        {
          name: "Sun",
          isActive: false,
          isDisabled: true,
        },
        {
          name: "Mon",
          isActive: false,
          isDisabled: false,
        },
        {
          name: "Tue",
          isActive: true,
          isDisabled: false,
        },
        {
          name: "Wed",
          isActive: false,
          isDisabled: false,
        },
        {
          name: "Thu",
          isActive: false,
          isDisabled: false,
        },
        {
          name: "Fri",
          isActive: false,
          isDisabled: false,
        },
        {
          name: "Sat",
          isActive: false,
          isDisabled: true,
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300&display=swap");

.сard {
  height: 575px;
  width: 370px;
  background-color: #fff;
  box-shadow: 0 2px 20px 0 rgba(0, 0, 0, 0.15);
  margin-top: -230px;
  padding: 32px 28px;

  .header {
    font-family: Quicksand;
    font-size: 24px;
    font-weight: bold;
    text-align: center;
    margin-bottom: 28px;
  }

  .recording {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 30px;

    span {
      font-family: Lato;
      font-size: 18px;
      font-weight: bold;
    }
  }

  @media (max-width: 1024px) {
    width: 356px;
    margin-top: -70px;
  }
}
</style>