<template>
  <!-- --------- Home -->

  <section class="home d-flex align-items-center">
    <Effects></Effects>
    <div class="container">
      <div class="row align-items-center">
        <div class="col-md-7">
          <div class="home-text">
            <h1>{{ title }}</h1>
            <p>
              {{ text }}
            </p>
            <div class="home-btn">
              <a href="" class="btn btn-1">download app</a>
              <button class="btn btn-1 video-play-btn">
                <i class="fas fa-play"></i>
              </button>
            </div>
          </div>
        </div>
        <div class="col-md-5 text-center">
          <div class="home-img">
            <div class="circle"></div>
            <img src="@/assets/img/app-screenshots/1.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- --------- Home -->
</template>

<script>
import Effects from "./Common/Animation";
export default {
  components: {
    Effects,
  },
  data() {
    return {
      title: "Best Mobile App Template for your Business",
      text: `Lorem ipsum dolor sit amet consectetur, adipisicing elit. Officiis
              expedita maxime voluptatum quisquam dolor aspernatur?`,
    };
  },
};
</script>

<style lang="scss" scoped>
/* ------------- Home */
.home {
  min-height: 100vh;
  padding: 150px 0;
  background: var(--main-to-dark-color);
  /* background: var(--main-color); */
  border-radius: 0 0 200px 0;
  position: relative;
  z-index: 1;
  overflow-x: hidden;
}
.home-text h1 {
  font-size: 45px;
  font-weight: 700;
  color: #fff;
  margin: 0 0 20px;
}
.home-text p {
  font-size: 18px;
  line-height: 28px;
  color: #fff;
  margin: 0;
  font-weight: 300;
}
.home .home-btn {
  margin-top: 40px;
}
.home .home-btn .video-play-btn {
  margin-left: 30px;
  height: 50px;
  width: 50px;
  padding: 0;
  animation: pulse_01 2s ease infinite;
  font-size: 16px;
}
.home .home-btn .video-play-btn:hover {
  animation: none;
  box-shadow: var(--shadow-300);
}
.home .home-btn .video-play-btn i {
  line-height: 50px;
}
.home-img img {
  max-width: 250px;
  width: 100%;
  box-shadow: var(--shadow-100);
  border-radius: 32px;
  animation: bounceTop_01 3s ease infinite;
}
.home-img {
  position: relative;
}
.home-img .circle {
  position: absolute;
  z-index: 1;
  height: 400px;
  width: 400px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.home-img .circle::before {
  content: "";
  position: absolute;
  height: 60px;
  width: 60px;
  background: rgba(255, 255, 255, 0.4);
  border-radius: 50%;
  left: 30px;
  top: 30px;
  transform-origin: 170px 170px;
  animation: spin_01 10s linear infinite;
}
/* ------------- Home */
</style>
