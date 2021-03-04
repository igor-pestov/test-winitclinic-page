<template>
  <div class="doctor">
    <header>
      <div class="up_header">
        <div class="alignment">
          <div class="breadcrumb">
            Homepage > Our health pros <span> > Dr.Sheila Woodhouse</span>
          </div>
          <div class="personal">
            <img class="avatar" src="@/assets/images/reviews/Ashley-L.jpg" />
            <div class="data">
              <span class="name">Dr. Sheila Woodhouse</span>
              <span class="position">OTOLARYNGOLOGYST</span>
            </div>
          </div>
        </div>
      </div>
      <div class="down_header">
        <div class="alignment">
          <div class="evaluation">
            4.6
            <img
              class="star"
              src="@/assets/images/star.svg"
              v-for="star of 5"
              :key="star"
            />
          </div>
          <div class="working">
            <span>
              <img src="@/assets/images/icon-location.svg" /> Los Angeles CA
            </span>
            <span>
              <img src="@/assets/images/icon-clock.svg" /> 15 min, 30 min, 45
              min, 1 hour
            </span>
            <span>
              <img src="@/assets/images/benefits/card.svg" /> $40 - $80
            </span>
          </div>
        </div>
      </div>
    </header>
    <section class="doctor_content">
      <div class="left">
        <Information v-bind:data="about" />
        <Education />
        <Information v-bind:data="languages" />
        <List v-bind:data="tests" />
        <List v-bind:data="symptoms" />
        <List v-bind:data="conditions" />
        <List v-bind:data="goals" />
        <div class="information_reviews">
          <h1>Reviews</h1>
          <Review
            v-for="(review, i) in reviews"
            :key="i"
            v-bind:data="review"
          />
        </div>
      </div>
      <div class="right">
        <Calendar />
      </div>
    </section>
  </div>
</template>

<script>
import Calendar from "../Calendar";
import Information from "./Information";
import List from "./List";
import Review from "./Review";
import Education from "./Education";

export default {
  components: {
    Calendar,
    Information,
    List,
    Review,
    Education,
  },
  data() {
    return {
      about: {
        heading: "About",
        text: `I am a Licensed Marriage and Family Therapist, a Registered Art
            Therapist, and a Board Ceftified Clinical Hypnotherapist. My
            approach is attachment-based/ Emotionally Focused Therapy (EFT) and
            I am trained in several other modalities such as Cognitive
            Behavioral Therapy (CBT), Dialectical Behavioral Therapy (DBT), and
            Mindfulness. But I customize each treatment based on my clients'
            needs. I am currently in the process of getting certified in Sex
            Therapy and EFT (Emotionally Focused Therapy).`,
      },
      languages: {
        heading: "Languages spoken",
        text: "English, Spanish",
      },
      tests: {
        heading: "Health tests",
        icon: "ds-height",
        content: [
          "Hormone Test",
          "Fungal Antibodies Test",
          "Neurotransmitter Test",
          "Enviromental Toxins Test",
          "Mycotoxins Test",
          "Gut Zoomer",
          "Heavy Metals Test",
        ],
      },
      symptoms: {
        heading: "Symptoms",
        icon: "ds-symptoms",
        content: [
          "Abdominal pain",
          "Acne",
          "Constipation",
          "Blurred vision",
          "Diarrhea",
          "Difficult paying attention",
          "Difficulty breathing",
          "Difficulty swallowing",
          "Distended stomach",
          "Dizziness",
          "Dry eyes",
          "Fever",
          "Lightheadedness",
          "Loss of coordination",
        ],
      },
      conditions: {
        heading: "Conditions",
        icon: "ds-conditions",
        content: [
          "Abnormally excessive sweating",
          "Acid reflux",
          "Actinic keratosis",
          "Acute respiratory distress syndrome",
          "ADHD in children",
          "ADHD, Adult",
          "Delayed sleep phase",
          "Diabetes, type 1",
          "Diabetes, type 2",
          "Diabetes, type 2",
        ],
      },
      goals: {
        heding: "Health goals",
        icon: "ds-goals",
        content: [
          "Get adequate rest daily",
          "Get regular physical activity",
          "Eat more plant based foods",
          "Eat more whole-grain breads and cereals",
          "Choose healthy fats",
          "Achieve/Maintain a healthy weight",
          "Be free of dependence on tobacco, illicit drugs, or alcohol",
          "Log Three Meals a Day",
          "Practice Portion Control",
          "Establishing a Morning Routine",
        ],
      },
      reviews: [
        {
          name: "Marianne M.",
          text:
            "I was starting to feel really overwhelmed by a plethora of different circumstances in my life, Sheila was a great help. She is calm and listened to what I was going through. Teresa helped me organize my thoughts and I’m very grateful.",
        },
        {
          name: "Jennifer F.",
          text:
            "Dr. Woodhouse has been a tremendous help! I wish I would've seeked out therapy sooner! When I tell her what I'm going through, she thoroughly listens and is able to give me a different way of approaching things when what I'm doing currently isn't working or is causing chaos or havoc. Sheila also shows care and genuine interest in helping which is such a comforting feeling.",
        },
        {
          name: "Tracey T.",
          text:
            "I was starting to feel really overwhelmed by a plethora of different circumstances in my life, Sheila was a great help. She is calm and listened to what I was going through. Sheila helped me organize my thoughts and I’m very grateful.",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300&display=swap");

.doctor {
  font-family: "Quicksand", sans-serif;
  header {
    .alignment {
      width: 80%;
      margin: 0 auto;
    }

    .up_header {
      width: 100%;
      height: 180px;
      padding-top: 25px;
      background: linear-gradient(
        0.25turn,
        #6c15cc,
        #8815c7 30%,
        #5a1ad8 70%,
        #631ccc
      );

      .breadcrumb {
        color: #fff;
        font-family: Lato;
        font-size: 17px;
        letter-spacing: 0.2px;
        line-height: 22px;

        span {
          color: #afafaf;
        }
      }

      .personal {
        display: flex;
        margin-top: 40px;

        .avatar {
          border-radius: 100%;
          width: 190px;
        }

        .data {
          display: flex;
          flex-direction: column;
          color: #fff;
          margin-left: 50px;
          font-weight: bold;

          .name {
            font-size: 32px;
          }

          .position {
            font-family: Lato;
            margin-top: 16px;
            letter-spacing: 1.6px;
          }
        }
      }
    }

    .down_header {
      width: 100%;
      height: 140px;
      background-color: #e6deee;
      padding-bottom: 15px;

      .alignment {
        display: flex;
        align-items: flex-end;
        height: 100%;

        .evaluation {
          display: flex;
          width: 190px;
          justify-content: center;
          align-items: center;

          .star {
            width: 15px;
            height: 15px;
            margin-left: 5px;
          }
        }

        .working {
          display: flex;
          flex-direction: column;
          color: #7a27c5;
          font-size: 17px;
          margin-left: 50px;
          font-family: Lato;

          span {
            display: flex;
            align-items: center;
            margin-top: 14px;

            img {
              width: 15px;
              margin-right: 10px;
            }
          }
        }
      }
    }
  }

  .doctor_content {
    width: 80%;
    display: flex;
    justify-content: center;
    margin: 0 auto;

    .left {
      width: 50%;

      .information_reviews {
        margin-top: 60px;

        h1 {
          margin-bottom: 31px;
        }
      }
    }

    .right {
      display: flex;
      justify-content: flex-end;
      width: 50%;
    }
  }
}

@media (max-width: 1024px) {
  .doctor {
    background-color: #fff;
    header {
      .up_header {
        background: #6c17ba;
        height: 270px;
        margin-top: 69px;

        .breadcrumb {
          font-size: 15px;
          width: 65%;
        }

        .personal {
          flex-direction: column-reverse;
          align-items: center;

          .avatar {
            width: 150px;
            margin-top: 25px;
          }

          .data {
            margin: 0;
            align-items: center;

            .name {
              font-size: 26px;
            }

            .position {
              margin-top: 10px;
            }
          }
        }
      }

      .down_header {
        height: 320px;
        background-color: #f1e9f9;

        .alignment {
          flex-direction: column;
          align-items: flex-start;
          padding-top: 90px;
          width: 90%;

          .evaluation {
            width: 100%;
          }

          .working {
            margin: 0;
            margin-top: 15px;

            span {
              font-size: 15px;

              img {
                width: 13px;
              }
            }
          }
        }
      }
    }

    .doctor_content {
      flex-direction: column-reverse;
      width: 95%;

      .right {
        width: 100%;
        justify-content: center;
      }

      .left {
        width: 95%;
        margin: 0 auto;
      }
    }
  }
}
</style>