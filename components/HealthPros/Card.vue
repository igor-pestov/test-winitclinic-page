<template>
  <div>
    <div class="healthPros__content_right_medic-1" @click.prevent="doctor">
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
      <div class="main_info">
        <div class="name-and-county">
          <p class="name">Name LastName</p>
          <p class="country">Los Angeles, CA</p>
        </div>
        <div class="position">Medic</div>
        <div class="about">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui sed iusto
          eius, ut, hic eum ratione error provident iure doloribus aut vel
          recusandae, praesentium non fugiat culpa adipisci consequuntur neque.
        </div>
      </div>
      <div class="consultation">
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
import ContentJob from './ContentJob'
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
.healthPros__content_right_medic-1 {
  padding: 15px;
  margin-bottom: 12px;
  .avatar {
    margin-right: 19px;
    display: flex;
    flex-direction: column;
    width: 100px;
    align-items: center;

    img {
      width: 60px;
      border-radius: 100%;
    }

    span {
      img {
        width: 12px;
        height: 12px;
        margin-right: 1px;
      }
    }
  }
  display: flex;
  justify-content: space-between;
  background-color: white;
  box-shadow: 0 4px 10px 0 rgba(0, 0, 0, 0.05);
}
</style>