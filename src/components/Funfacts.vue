<template>
  <section class="fun_facts section_padding">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 col-md-5 d-flex align-items-center">
          <div class="fun_facts_img">
            <img src="@/assets/img/app-screenshots/2.png" alt="" />
          </div>
        </div>
        <div class="col-lg-6 col-md-7">
          <div class="section_title">
            <h2>fun <span>facts</span></h2>
          </div>
          <div class="fun_facts_text">
            <p>
              {{ text }}
            </p>

            <div class="row">
              <div class="col-sm-6" v-for="(fact, i) in facts" :key="i">
                <div :class="['fun_fact_item', fact.class]">
                  <h3>{{ fact.heading }}</h3>
                  <span>{{ fact.text }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      facts: [
        {
          heading: "4000",
          text: `downloads`,
          class: "style_1",
        },
        {
          heading: "4000",
          text: `downloads`,
          class: "style_2",
        },
        {
          heading: "4000",
          text: `downloads`,
          class: "style_3",
        },
        {
          heading: "4000",
          text: `downloads`,
          class: "style_4",
        },
      ],
      text: ` Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore
              voluptatum suscipit obcaecati molestiae accusantium sit?`,
    };
  },
};
</script>

<style lang="scss" scoped>
/* -------------  Features */

.fun_facts {
  background-color: var(--black-100);
}
.fun_facts .section_title {
  margin-bottom: 20px;
}
.fun_facts .section_title h2 {
  text-align: left;
}
.fun_facts_img img {
  max-width: 250px;
  width: 100%;
  box-shadow: var(--shadow-100);
  border-radius: 32px;
  animation: bounceTop_01 3s ease infinite;
}
.fun_facts_text p {
  font-size: 16px;
  line-height: 26px;
  color: var(--black-400);
  margin: 0 0 15px;
  font-weight: 300;
}

.fun_fact_item {
  padding: 30px;
  text-align: center;
  box-shadow: var(--shadow-100);
  border-radius: 10px;
  margin-top: 30px;
  color: #fff;
}
.fun_facts_item h3 {
  font-size: 40px;
  font-weight: 700;
  color: #fff;
  margin: 0 0 8px;
}
.fun_fact_item span {
  font-size: 16px;
  line-height: 26px;
  text-transform: uppercase;
  font-weight: 300;
  margin: 0;
  display: block;
}
.fun_fact_item.style_1 {
  background-color: var(--color-1);
}
.fun_fact_item.style_2 {
  background-color: var(--color-2);
}
.fun_fact_item.style_3 {
  background-color: var(--color-3);
}
.fun_fact_item.style_4 {
  background-color: var(--main-color);
}
</style>
