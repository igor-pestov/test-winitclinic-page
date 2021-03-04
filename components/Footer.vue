<template>
  <div class="footer">
    <div class="footer__container">
      <div class="footer__container_columnInfo">
        <img src="../assets/images/footer/footer-logo.png" alt="" />
        <p>About us</p>
        <p>Register Kit</p>
        <p>Privacy Policy</p>
        <p>Terms of Service</p>
        <h4>2020 © WINIT</h4>
      </div>
      <div class="footer__container_columnSymptoms">
        <h3>Symptoms</h3>
        <p>Anxiety</p>
        <p>Bloating</p>
        <p>Diabetes</p>
        <p>Chronic Fatigue Syndrome</p>
        <p>Headaches</p>
        <p>Brain fog</p>
        <p>Muscle/Joint weaknes</p>
      </div>
      <div class="footer__container_columnHealthGoals">
        <h3>Health goals</h3>
        <p>Gain mental clarity</p>
        <p>Lose weight</p>
        <p>Get better sleep</p>
        <p>Strengthen immune system</p>
        <p>Build muscle</p>
        <p>Gain more energy</p>
        <p>Be happy</p>
      </div>
      <div class="footer__container_columnMedConditions">
        <h3>Medical conditions</h3>
        <p>Allergies</p>
        <p>Alzheimer`s Disease</p>
        <p>Cancer</p>
        <p>Depression</p>
        <p>Obesity</p>
        <p>Hypertension</p>
        <p>Heart Disease</p>
      </div>
      <div class="footer__container_columnAutoDiseases">
        <h3>Auto-immune diseases</h3>
        <p>Type 1 diabets</p>
        <p>Rheumatoid Arthritis</p>
        <p>Lupus</p>
        <p>Inflammatory Bowel Disease</p>
        <p>Multiple sclerosis</p>
        <p>Psoriasis</p>
        <p>Hashimoto`s Thyroiditis</p>
      </div>
      <div class="footer__container_columnContact">
          <div class="footer__container_columnContact-phone">
        <img src="@/assets/images/icon-phone.svg" alt="" />
        <p>323 401 1535</p>
        </div>
        <img class="stores" src="@/assets/images/footer/google-play.png" alt="">
        <img class="stores" src="@/assets/images/footer/app-store.png" alt="">
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>

<style lang="scss">
.footer {
  background-color: #0d0044;
  width: 100%;
  color: white;
  .footer__container {
    display: flex;
    max-width: 1200px;
    margin: 0 auto;
    padding: 88px 0px;
    justify-content: space-between;
    font-size: 14px;
    line-height: 25px;
        div{
            width: 16%;
            
        }
    .footer__container_columnInfo{
        img{
            width: 130px;
            margin-bottom: 20px;
            
        }
        h4{
            margin-top: 20px;
        }
    }
    .footer__container_columnContact{
        .stores{
            width: 100%;
            margin-top: 10px;
        }
        .footer__container_columnContact-phone{
            display: flex;
            flex-direction: row;
            border: 1px solid #706991;
            padding: 13px;
            border-radius: 25px;
            width: 100%;
           
        }
    }
  }
}
</style>