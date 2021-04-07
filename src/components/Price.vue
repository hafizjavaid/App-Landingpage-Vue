<template>
  <!-- --- Price Section -->
  <section class="price section_padding">
    <div class="container">
      <Title :text1="text1" :text2="text2" :text3="text3"></Title>
      <div class="row">
        <div class="col-lg-4 col-md-6" v-for="price in pricing" :key="price.type">
          <div class="pricing_plan">
            <div class="pricing_header">
              <h3>{{price.type}}</h3>
            </div>
            <div class="pricing_price">
              <span class="currency">$</span>
              <span class="price">{{price.price}}</span>
              <span class="period">{{price.cat}}</span>
            </div>
            <div class="pricing_body">
              <ul>
                <li v-for="(pricetext,j) in price.texts" :key="j">
                  <i :class="price.icon"> </i>
                 {{pricetext}}
                </li>
               
              </ul>
            </div>
            <div class="pricing_footer">
              <a href="" class="btn btn-2"> get started </a>
            </div>
          </div>
        </div>
    
      </div>
    </div>
  </section>
  <!-- --- Price Section -->
</template>

<script>
export default {
  data() {
    return {
      text1: "Pricing",
      text2: "Plan",
      text3: "",
      pricing:[
          {
              type:'Basic',
              price:'99',
              cat:'monthly',
              icon:'fas fa-check',
              texts:[' 5 GB Bandwidth',' 5 GB Bandwidth', ' 5 GB Bandwidth', ' 5 GB Bandwidth', ' 5 GB Bandwidth']
          },
           {
              type:'Monthly',
              price:'120',
              cat:'monthly',
              icon:'fas fa-check',
              texts:[' 5 GB Bandwidth',' 5 GB Bandwidth', ' 5 GB Bandwidth', ' 5 GB Bandwidth', ' 5 GB Bandwidth']
          },
           {
              type:'Yearly',
              price:'150',
              cat:'monthly',
              icon:'fas fa-check',
              texts:[' 5 GB Bandwidth',' 5 GB Bandwidth', ' 5 GB Bandwidth', ' 5 GB Bandwidth', ' 5 GB Bandwidth']
          },
      ]
    };
  },
};
</script>

<style lang="scss" scoped>
/* ======================= price Section */
.price {
}
.pricing_plan {
  box-shadow: var(--shadow-100);
  border-radius: 10px;
}
.pricing_plan .pricing_header {
  padding: 20px 30px;
  border-bottom: 1px solid var(--black-alpha-100);
}
.pricing_plan .pricing_header h3 {
  text-align: center;
  font-size: 30px;
  color: var(--black-900);
  font-weight: 500;
  text-transform: capitalize;
}
.pricing_plan .pricing_price {
  padding: 40px 30px;
  display: flex;
  justify-content: center;
  line-height: 0.7;
}
.pricing_plan .pricing_price .currency {
  font-size: 16px;
  font-weight: 300;
  color: var(--black-400);
  margin-right: 5px;
  align-self: flex-start;
}
.pricing_plan .pricing_price .price {
  font-size: 80px;
  font-weight: 700;
  color: var(--main-color);
}
.pricing_plan .pricing_price .period {
  font-size: 16px;
  font-weight: 300;
  color: var(--black-400);
  margin-right: 50px;
  align-self: flex-end;
  text-transform: uppercase;
  font-size: 14px;
}

.pricing_plan .pricing_body {
  padding: 0 30px;
}
.pricing_plan .pricing_body ul li {
  font-size: 16px;
  font-weight: 300;
  color: var(--black-400);
  padding: 10px 0 10px 30px;
  border-bottom: 1px solid var(--black-alpha-100);
  line-height: 26px;
  position: relative;
}
.pricing_plan .pricing_body ul li:last-child {
  margin-bottom: none;
  border-bottom: none;
}
.pricing_plan .pricing_body ul li i {
  position: absolute;
  color: var(--main-color);
  left: 0;
  top: 10px;
}
.pricing_plan .pricing_footer {
  padding: 20px 30px 30px;
  text-align: center;
}

/* ======================= price Section */
</style>
