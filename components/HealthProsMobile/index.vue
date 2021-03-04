<template>
  <div class="healthProsMobile">
    <img class="back" src="@/assets/images/blured-background.svg" alt="" />
    <div class="content">
      <h2>WINIT Health pros</h2>
      <div class="healthProsMobile__sort">
        <Select
          v-for="(data, i) in selectData"
          :key="i"
          v-bind:heading="data.heading"
          v-bind:placeholder="data.placeholder"
          v-bind:close="data.close"
          v-bind:isClose="data.isClose"
        />
      </div>
      <Card v-for="doc of 10" :key="doc" v-bind:index="doc" />
      <ContentHelp />
    </div>
  </div>
</template>

<script>
import Select from "../Select";
import Card from "./Card";
import ContentHelp from "./ContentHelp";
export default {
  components: {
    Select,
    Card,
    ContentHelp,
  },
  data() {
    return {
      selectData: [
        {
          heading: "State",
          placeholder: "Select your option",
          close: false,
          isClose: true,
        },
        {
          heading: "Role",
          placeholder: "Select a role",
          close: true,
          isClose: false,
        },
        {
          heading: "Gender",
          placeholder: "Select a gender",
          close: true,
          isClose: false,
        },
        {
          heading: "Specialty",
          placeholder: "Select a Specialty",
          close: true,
          isClose: false,
        },
        {
          heading: "Experience",
          placeholder: "Select a Experience",
          close: true,
          isClose: false,
        },
        {
          heading: "Price range",
          placeholder: "Select a Price range",
          close: true,
          isClose: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.healthProsMobile {
  margin-top: 70px;
  .back {
    position: relative;
    top: 0px;
    width: 100%;
    height: 300px;
    filter: blur(10px);
  }
  .content {
    margin-top: -250px;
    h2 {
      padding: 50px;
      text-align: center;
      font-size: 30px;
      font-weight: bold;
    }
    .healthProsMobile__sort {
      width: 75%;
      margin: 0 auto;
      margin-bottom: 50px;
    }
  }
}
</style>