<template>
  <div class="healthPros">
    <div class="healthPros__header">
      <img src="@/assets/images/corner-left-lg-size.svg" alt="" />
      <h2>WINIT health pros</h2>
      <img src="@/assets/images/corner-right-lg-size.svg" alt="" />
    </div>
    <section class="healthPros__content">
      <div class="healthPros__content_left">
        <Select
          v-for="(data, i) in selectData"
          :key="i"
          v-bind:heading="data.heading"
          v-bind:placeholder="data.placeholder"
          v-bind:close="data.close"
          v-bind:isClose="data.isClose"
        />
      </div>
      <div class="healthPros__content_right">
        <Card v-for="doc of 10" :key="doc" v-bind:index="doc" />
        <ContentHelp />
      </div>
    </section>
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
          isClose: true,
        },
        {
          heading: "Gender",
          placeholder: "Select a gender",
          close: true,
          isClose: true,
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
.healthPros {
  margin-bottom: 40px;
  .healthPros__header {
    display: flex;
    justify-content: space-between;
    h2 {
      font-size: 40px;
      margin-top: 70px;
      font-family: "Quicksand", sans-serif;
    }
  }
  .healthPros__content {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    margin-top: -130px;

    .healthPros__content_left {
      width: 30%;

      margin-top: -30px;
      margin-right: 29px;
    }
    .healthPros__content_right {
      width: 70%;

      .main_info {
        width: 64%;
        .name-and-county {
          display: flex;
          .name {
            margin-right: 20px;
            margin-bottom: 12px;
            font-weight: bold;
          }
          .country {
            color: #7a25cb;
            margin-bottom: 12px;
            cursor: pointer;
          }
        }
        .position {
          font-size: 12px;
          font-weight: bold;
          margin-bottom: 12px;
        }
      }
      .consultation {
        .price {
          display: flex;
          font-weight: bold;
          margin-bottom: 12px;
          img {
            margin-top: 3px;
            margin-right: 10px;
          }
        }
        .view {
          cursor: pointer;
          display: flex;
          p {
            font-weight: bold;
            color: #7a25cb;
            margin-right: 10px;
          }
          img {
            margin-top: 3px;
          }
        }
      }
    }
  }
}
</style>