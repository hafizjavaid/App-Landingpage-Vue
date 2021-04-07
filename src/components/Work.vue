<template>
  <!-- -- Work Section -->
  <section class="h_works section_padding">
    <div class="container">
      <Title :text1="text1" :text2="text2" :text3="text3"></Title>
      <div class="row">
    
        <div class="col-lg-3 col-md-6" v-for="work in works" :key="work.id">
          <div :class="['h_works_item', work.class]">
            <div class="step">{{work.id}}</div>
            <h3>{{work.text}}</h3>
            <p>
              {{work.desc}}
            </p>
          </div>
        </div>
     
      </div>
    </div>
  </section>
  <!-- -- Work Section -->
</template>

<script>
import Title from "./Common/Title";

export default {
  data() {
    return {
      text1: "how it",
      text2: "works",
      text3: "",
      works:[
          {
              id:1,
              text: "download",
              desc:` Lorem ipsum dolor sit amet consectetur, adipisicing elit. Maiores
              rem eius et modi, vel dolorem asperiores amet cumque laboriosam
              eum?`,
              class:'line_right'
          },
          {
              id:2,
              text: "download",
              desc:` Lorem ipsum dolor sit amet consectetur, adipisicing elit. Maiores
              rem eius et modi, vel dolorem asperiores amet cumque laboriosam
              eum?`,
              class:'line_right'
          },
          {
              id:3,
              text: "download",
              desc:` Lorem ipsum dolor sit amet consectetur, adipisicing elit. Maiores
              rem eius et modi, vel dolorem asperiores amet cumque laboriosam
              eum?`,
              class:'line_right'
          },
          {
              id:4,
              text: "download",
              desc:` Lorem ipsum dolor sit amet consectetur, adipisicing elit. Maiores
              rem eius et modi, vel dolorem asperiores amet cumque laboriosam
              eum?`,
              class:''
          },
      ]
    };
  },
  components: {
    Title,
  },
};
</script>

<style lang="scss" scoped>
/* ======================= Works How */
.h_works_item {
  padding: 30px;
  text-align: center;
  box-shadow: var(--black-100);
  position: relative;
  z-index: 1;
}
.h_works_item.line_right::before {
  content: "";
  position: absolute;
  height: 2px;
  width: 100%;
  left: 50%;
  top: 60px;
  background-color: var(--main-color);
  z-index: -1;
}
.h_works_item .step {
  display: inline-block;
  height: 60px;
  width: 60px;
  border-radius: 50%;
  background-color: var(--main-color);
  font-size: 30px;
  text-align: center;
  line-height: 60px;
  color: #fff;
  font-weight: 500;
  margin: 0 0 15px;
}
.h_works_item h3 {
  font-size: 22px;
  color: var(--black-900);
  margin: 20px 0;
  font-weight: 500;
  text-transform: capitalize;
}
.h_works_item p {
  font-size: 16px;
  color: var(--black-400);
  font-weight: 300;
  margin: 0 0 30px;
  line-height: 26px;
}

@media(max-width: 991px)
{
     .h_works_item.line_right::before {
    content: none;
  }
  .h_works_item {
    box-shadow: var(--shadow-100);
    border-radius: 10px;
  }
}

/* ======================= Works How */
</style>
