<template>
  <div>
    <div @click.prevent="doctor" class="healthProsMobile__doctors">
      <div class="healthProsMobile__doctors_row-1">
        <div class="avatar">
          <img src="@/assets/images/reviews/Ashley-L.jpg" alt="error" />
          <span
            ><img
              src="@/assets/images/star.svg"
              alt="error"
              v-for="star in 5"
              :key="star"
          /></span>
        </div>

        <div class="healthProsMobile__doctors_row-1-mainInfo">
          <div class="name">Name LastName</div>
          <div class="country">Los Angeles, CA</div>
          <div class="position">Medic</div>
        </div>
      </div>
      <div class="healthProsMobile__doctors_row-2">
        <div class="about">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident
          voluptatum libero eum dicta laudantium incidunt iusto sint nesciunt
          impedit fugit ullam laboriosam sunt iure quidem labore alias eaque,
          totam vero.
        </div>
      </div>
      <div class="healthProsMobile__doctors_row-3">
        <div class="price">
          <img src="@/assets/images/icon-payout.svg" alt="" />
          <p>$40-90</p>
        </div>
        <div class="view">
          <p>Book a consultation</p>
          <img src="@/assets/images/icon-chevron-right.svg" alt="" />
        </div>
      </div>
    </div>
    <ContentJob v-if="index === 5" />
  </div>
</template>

<script>
import ContentJob from "./ContentJob";
export default {
  components: {
    ContentJob,
  },
  props: {
    index: {
      type: Number,
    },
  },
  methods: {
    doctor() {
      this.$router.push("/doctor");
    },
  },
};
</script>

<style lang="scss" scoped>
.healthProsMobile__doctors {
  background-color: white;
  box-shadow: 0 4px 10px 0 rgba(0, 0, 0, 0.05);
  margin: 0 auto;
  padding: 20px 10px;
  margin-bottom: 15px;
  width: 90%;

  .healthProsMobile__doctors_row-1 {
    display: flex;

    .avatar {
      margin-right: 10px;
      display: flex;
      flex-direction: column;
      align-items: center;
      img {
        width: 60px;
        height: 60px;
        border-radius: 100%;
      }

      span {
        display: flex;
        margin-top: 5px;
        img {
          width: 13px;
          height: 13px;
          margin-right: 2px;
        }
      }
    }

    .healthProsMobile__doctors_row-1-mainInfo {
      div {
        line-height: 25px;
      }
      .name {
        font-weight: bold;
      }
      .country {
        color: #7a25cb;
      }
      .position {
        font-weight: bold;
        font-size: 14px;
      }
    }
  }
  .healthProsMobile__doctors_row-2 {
    margin-top: 15px;
    .about {
      line-height: 23px;
      font-weight: 300;
    }
  }
  .healthProsMobile__doctors_row-3 {
    .price {
      margin-top: 15px;
      display: flex;
      img {
        margin-right: 10px;
      }
    }
    .view {
      margin-top: 15px;
      display: flex;
      p {
        margin-right: 15px;
        color: #7a25cb;
      }
      img {
        margin-top: 5px;
      }
    }
  }
}
</style>