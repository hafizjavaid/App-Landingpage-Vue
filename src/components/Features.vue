<template>
  <!-- --------- Features -->
  <section class="features section_padding">
    <div class="container">
      <Title :text1="text1" :text2="text2" :text3="text3"></Title>
      <div class="row">
        <div
          class="col-lg-4 col-md-6"
          v-for="feature in features"
          :key="feature.icon"
        >
          <div class="feature_item">
            <div class="icon">
              <i :class="feature.icon"></i>
            </div>
            <h3>{{ feature.heading }}</h3>
            <p>
              {{ feature.text }}
            </p>
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
      text1: "awesome",
      text2: "fetures",
      text3: "",
      features: [
        {
          icon: "fas fa-code",
          heading: "clean code",
          text: ` Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                Accusantium, tempore earum reiciendis inventore laboriosam amet.`,
        },
        {
          icon: "fas fa-edit",
          heading: "auto install system",
          text: ` Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                Accusantium, tempore earum reiciendis inventore laboriosam amet.`,
        },
        {
          icon: "fas fa-paint-brush",
          heading: "clean code",
          text: ` Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                Accusantium, tempore earum reiciendis inventore laboriosam amet.`,
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
/* -------------  Features */

.features .feature_item {
  box-shadow: var(--shadow-100);
  margin: 15px 5px;
  padding: 30px;
  border-radius: 10px;
  text-align: center;
  position: relative;
  z-index: 1;
  overflow: hidden;
}
.features .feature_item::before,
.features .feature_item::after {
  content: "";
  position: absolute;
  z-index: -1;
  border-radius: 50%;
  transition: 0.5s ease;
  opacity: 0;
}
.features .feature_item::before {
  height: 20px;
  width: 20px;
  background-color: var(--color-1);
  left: -20px;
  top: 40%;
}
.features .feature_item:hover::before {
  left: 10px;
  opacity: 1;
}

.features .feature_item:hover::after {
  right: -15px;
  opacity: 1;
}

.features .feature_item::after {
  height: 30px;
  width: 30px;
  background-color: var(--color-2);
  right: -30px;
  top: 80%;
}
.features .feature_item .icon {
  height: 60px;
  width: 60px;
  margin: 0 auto 30px;
  text-align: center;
  /* background-color: red; */
  font-size: 30px;
  color: var(--main-color);
  position: relative;
  z-index: 1;
}
.features .feature_item .icon::before {
  content: "";
  position: absolute;
  left: 0%;
  /* Or */
  left: 100%;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: var(--main-color);
  transition: 0.5s ease;
  z-index: -1;
  opacity: 0;
  border-radius: 50%;
}
.features .feature_item:hover .icon {
  color: #ffffff;
  font-size: 20px;
}
.features .feature_item:hover .icon::before {
  left: 0;
  border-radius: 50%;
  opacity: 1;
}
.features .feature_item .icon i {
  line-height: 60px;
}
.features .feature_item h3 {
  font-size: 22px;
  margin: 0 0 20px;
  color: var(--black-900);
  font-weight: 500;
  text-transform: capitalize;
}

.features .feature_item p {
  font-size: 16px;
  line-height: 26px;
  font-weight: 300;
  color: var(--black-400);
  margin: 0 0 15px;
}
</style>
