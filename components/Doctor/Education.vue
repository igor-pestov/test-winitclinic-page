<template>
  <div class="information">
    <div class="education">
      <h1>Education</h1>
      <div class="block">
        <img src="@/assets/images/account/icon-result.svg" />
        <div>
          <span class="year">2014</span>
          <span class="city">UC Berkeley</span>
          <span class="profession">Marriage and Family Therapist</span>
        </div>
      </div>
    </div>
    <div class="certifications">
      <h1>Notable certifications</h1>
      <div class="block">
        <img src="@/assets/images/account/icon-result.svg" />
        <div>
          <span class="year">2014</span>
          <span class="city">UC Berkeley</span>
          <span class="profession">Marriage and Family Therapist</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.information {
  margin-top: 44px;
  display: flex;
  justify-content: space-between;
  width: 85%;

  .education,
  .certifications {
    .block {
      display: flex;
      width: 300px;
      justify-content: space-around;
      align-items: center;
      margin-top: 24px;

      img {
        width: 29px;
        height: 34px;
      }

      div {
        display: flex;
        flex-direction: column;

        span {
          margin-top: 5px;
        }

        .year {
          color: rgba(132, 132, 132, 1);
          font-family: Lato;
          font-size: 16px;
        }

        .city {
          color: rgba(51, 51, 51, 1);
          font-family: Lato;
          font-size: 16px;
          font-weight: bold;
        }

        .profession {
          color: rgba(51, 51, 51, 1);
          font-family: Lato;
          font-size: 16px;
        }
      }
    }
  }
  @media (max-width: 1024px) {
    width: 100%;
    flex-direction: column;

    .certifications {
      margin-top: 20px;
    }
  }
}
</style>