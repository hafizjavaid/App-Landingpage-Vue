<template>
  <!-- --------- Features -->
  <section class="app_screens section_padding">
    <div class="container">
      <Title :text1="text1" :text2="text2" :text3="text3"></Title>
      <div class="row">
        <div
          class="col-lg-3 col-md-4 col-sm-6"
          v-for="(screen, i) in screens"
          :key="i"
        >
          <div class="screen_item">
            <img :src="screen.img" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- --------- Features -->
</template>

<script>
import Title from "./Common/Title";
export default {
  data() {
    return {
      text1: "App",
      text2: "Screenshots",
      text3: "",
      screens: [
        {
          img: require("@/assets/img/app-screenshots/1.png"),
        },
        {
          img: require("@/assets/img/app-screenshots/2.png"),
        },
        {
          img: require("@/assets/img/app-screenshots/3.png"),
        },
        {
          img: require("@/assets/img/app-screenshots/1.png"),
        },
      ],
    };
  },
  components: {
    Title,
  },
};
</script>

<style lang="scss" scoped>
/* -------------  Screens */
.screen_item {
  margin: 15px;
}
.screen_item img {
  width: 100%;
  max-width: 250px;
  display: block;
  margin: auto;
}
</style>
