<template>
  <div class="user_review">
    <div class="pacient">
      <span>{{ data.name }}</span>
      <span>
        <img
          class="star"
          src="@/assets/images/star.svg"
          v-for="star of 5"
          :key="star"
        />
      </span>
    </div>
    <div class="review">
      {{ data.text }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
      requred: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.user_review {
  display: flex;
  font-family: Lato;
  font-size: 16px;
  font-weight: bold;
  letter-spacing: 0.2px;
  padding: 16px 0;
  border-bottom: 1px solid rgba(212, 212, 212, 1);

  .pacient {
    display: flex;
    flex-direction: column;
    width: 120px;

    span {
      display: flex;
      margin-bottom: 12px;
      line-height: 22px;

      img {
        width: 16px;
        height: 16px;
      }
    }
  }

  .review {
    width: 65%;
    font-family: Lato;
    font-size: 16px;
    letter-spacing: 0.2px;
    line-height: 22px;
    font-weight: 500;
  }

  @media (max-width: 1024px) {
    flex-direction: column;

    .pacient {
      span {
        margin-bottom: 10px;

        img {
          width: 13px;
          height: 13px;
          margin-right: 3px;
        }
      }
    }

    .review {
      width: 100%;
    }
  }
}
</style>