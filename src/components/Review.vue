<template>
  <!-- -- Team Section -->
  <section class="review section_padding">
    <div class="container">
      <Title :text1="text1" :text2="text2" :text3="text3"></Title>
      <div class="row">
        <div
          class="col-lg-3 col-md-4 col-sm-6"
          v-for="review in reviews"
          :key="review.img"
        >
          <div class="review_item">
            <div class="img_box">
              <img :src="review.img" alt="" />
              <i :class="review.icon"></i>
            </div>
            <p>
              {{ review.desc }}
            </p>
            <h3>{{ review.namee }}</h3>
            <span>{{ review.cat }}</span>
            <div class="rating">
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- -- Team Section -->
</template>

<script>
import Title from "./Common/Title";

export default {
  data() {
    return {
      text1: "What Our",
      text2: "Client",
      text3: "say",
      reviews: [
        {
          img: require("@/assets/img/testimonial/1.jpg"),
          icon: "fas fa-quote-right",
          desc: ` Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum ipsa
              impedit itaque laborum nam iure.`,
          namee: "Hafiz Javaid",
          cat: "UI Developer",
        },
        {
          img: require("@/assets/img/testimonial/2.jpg"),
          icon: "fas fa-quote-right",
          desc: ` Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum ipsa
              impedit itaque laborum nam iure.`,
          namee: "Hafiz Javaid",
          cat: "UI Developer",
        },
        {
          img: require("@/assets/img/testimonial/3.jpg"),
          icon: "fas fa-quote-right",
          desc: ` Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum ipsa
              impedit itaque laborum nam iure.`,
          namee: "Hafiz Javaid",
          cat: "UI Developer",
        },
        {
          img: require("@/assets/img/testimonial/4.jpg"),
          icon: "fas fa-quote-right",
          desc: ` Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum ipsa
              impedit itaque laborum nam iure.`,
          namee: "Hafiz Javaid",
          cat: "UI Developer",
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
/* ======================= Team Section */
.review {
  background-color: var(--black-100);
}
.review_item {
  // margin: 15px;
  padding: 30px;
  box-shadow: var(--shadow-100);
  border-radius: 10px;
  text-align: center;
}
.review_item .img_box {
  height: 100px;
  width: 100px;
  display: inline-block;
  margin-bottom: 30px;
  border: 4px solid var(--main-color);
  border-radius: 50%;
  position: relative;
}
.review_item .img_box img {
  border-radius: 50%;
  width: 100%;
}

.review_item .img_box i {
  position: absolute;
  height: 30px;
  width: 30px;
  background-color: var(--main-color);
  border-radius: 50%;
  text-align: center;
  color: #fff;
  line-height: 30px;
  left: calc(100% - 15px);
  top: calc(50% - 15px);
}
.review_item p {
  font-size: 16px;
  color: var(--black-400);
  font-weight: 300;
  margin: 0 0 20px;
  line-height: 26px;
}
.review_item h3 {
  font-size: 22px;
  color: var(--black-900);
  margin: 20px 0;
  font-weight: 500;
  text-transform: capitalize;
  margin: 0 0 5px;
}
.review_item span {
  display: block;
  font-size: 16px;
  color: var(--black-400);
  font-weight: 300;
}
.review_item .rating {
  margin-top: 10px;
}

.review_item .rating i {
  /* margin-top: 10px;
     */
  display: inline-block;
  font-size: 16px;
  color: var(--color-2);
}

/* ======================= Team Section */
</style>
