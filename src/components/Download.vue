<template>
  <!-- Download Section -->
  <section class="app_download section_padding">
    <div class="container">
      <Title :text1="text1" :text2="text2" :text3="text3"></Title>
      <div class="row justify-content-center">
        <div
          class="col-lg-4 col-md-6"
          v-for="download in downloads"
          :key="download.icon"
        >
          <div class="app_download_item">
            <i :class="download.icon"></i>
            <h3>{{ download.text }}</h3>
            <p>
              {{ download.desc }}
            </p>
            <a href="" class="btn btn-2">dowload now</a>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- Download Section -->
</template>

<script>
import Title from "./Common/Title";
export default {
  data() {
    return {
      text1: "Download",
      text2: "App",
      text3: "",
      downloads: [
        {
          icon: "fab fa-apple",
          text: "google play",
          desc: `Lorem ipsum dolor, sit amet consectetur adipisicing elit. Non
              eveniet aut explicabo dicta sunt voluptas culpa voluptatum autem
              accusantium blanditiis!`,
        },
        {
          icon: "fab fa-google-play",
          text: "google play",
          desc: `Lorem ipsum dolor, sit amet consectetur adipisicing elit. Non
              eveniet aut explicabo dicta sunt voluptas culpa voluptatum autem
              accusantium blanditiis!`,
        },
        {
          icon: "fab fa-windows",
          text: "microsoft windows",
          desc: `Lorem ipsum dolor, sit amet consectetur adipisicing elit. Non
              eveniet aut explicabo dicta sunt voluptas culpa voluptatum autem
              accusantium blanditiis!`,
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
/* ======================= Download */

.app_download {
  background-image: url(../assets/img/download-app-bg.jpg);
  background-position: center top;
  background-attachment: fixed;
  position: relative;
  z-index: 1;
}
.app_download::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  /* z-index: -1; */
  background-color: var(--main-to-dark-color);
  opacity: 0.8;
}
.app_download .section_title h2 {
  color: #fff;
}
.app_download_item {
  background-color: var(--black-000);
  padding: 30px;
  text-align: center;
  border-radius: 10px;
  box-shadow: var(--black-100);
}
.app_download i {
  font-size: 30px;
  color: var(--main-color);
  display: inline-block;
}
.app_download h3 {
  font-size: 22px;
  color: var(--black-900);
  margin: 20px 0;
  font-weight: 500;
  text-transform: capitalize;
}
.app_download p {
  font-size: 16px;
  color: var(--black-400);
  font-weight: 300;
  margin: 0 0 30px;
  line-height: 26px;
}

/* ======================= Download */
</style>
