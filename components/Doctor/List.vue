<template>
  <div class="information">
    <h1>{{data.heading}}</h1>
    <ul>
      <li v-for="li of data.content" :key="li">
        <img :src="require(`@/assets/images/dashboard/${data.icon}.svg`)" /> {{li}}
      </li>
    </ul>
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
.information {
        width: 100%;
        margin-top: 52px;

        ul {
          margin-top: 20px;
          padding: 0;

          li {
            border-radius: 5px;
            background-color: rgba(239, 235, 243, 1);
            color: rgba(142, 0, 228, 1);
            font-family: Lato;
            font-size: 12px;
            font-weight: bold;
            letter-spacing: 0.15px;
            line-height: 22px;
            list-style-type: none;
            display: inline-flex;
            padding: 2px;
            margin-right: 5px;

            img {
              margin: 0 3px;
            }
          }
        }

        h1 {
          font-size: 24px;
          font-weight: bold;
          font-family: Quicksand;
        }
      }
</style>