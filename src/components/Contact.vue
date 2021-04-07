<template>
  <!-- ---- Contact Form -->
  <section class="contact section_padding">
    <div class="container">
      <Title :text1="text1" :text2="text2" :text3="text3"></Title>

      <div class="row">
        <div class="col-lg-4 col-md-5">
          <div class="contact_info">
            <h3>For Any Quries and Support</h3>
            <div
              class="contact_info_item"
              v-for="info in infos"
              :key="info.icon"
            >
              <i :class="info.icon"></i>
              <h3>{{ info.text }}</h3>
              <p>{{ info.des }}</p>
            </div>
          </div>
        </div>
        <div class="col-lg-8 col-md-7">
          <div class="contact_form">
            <form action="">
              <div class="row">
                <div class="col-lg-6">
                  <div class="form-group">
                    <input
                      type="text"
                      placeholder="Your Name"
                      class="form-control"
                    />
                  </div>
                </div>

                <div class="col-lg-6">
                  <div class="form-group">
                    <input
                      type="Email"
                      placeholder="Your Email"
                      class="form-control"
                    />
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-lg-12">
                  <div class="form-group">
                    <input
                      type="text"
                      placeholder="Your Phone"
                      class="form-control"
                    />
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-lg-12">
                  <div class="form-group">
                    <input
                      type="text"
                      placeholder="Your Subject"
                      class="form-control"
                    />
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-lg-12">
                  <div class="form-group">
                    <textarea
                      placeholder="Your Message"
                      class="form-control"
                    ></textarea>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-lg-12">
                  <button type="submit" class="btn btn-2">
                    Send Message
                  </button>
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- ---- Contact Form -->
</template>

<script>
import Title from "./Common/Title";
export default {
  data() {
    return {
      text1: "get in",
      text2: "touch",
      text3: "",
      infos: [
        {
          icon: "fas fa-location-arrow",
          text: "Company Location",
          des: "House 569, Islamabad",
        },
        {
          icon: "fas fa-envelope",
          text: "Write to us at",
          des: "info@gmail.com",
        },
        {
          icon: "fas fa-phone",
          text: "Call us on",
          des: "+92 345 7887703",
        },
      ],
      components: {
        Title,
      },
    };
  },
};
</script>

<style lang="scss" scoped>
/* ============= Contact */
.contact {
  background-color: var(--black-100);
}
.contact_info h3 {
  font-size: 22px;
  color: var(--black-900);
  font-weight: 500;
  margin: 0 0 40px;
}
.contact_info_item {
  position: relative;
  padding-left: 55px;
  margin-bottom: 30px;
}
.contact_info_item i {
  position: absolute;
  height: 40px;
  width: 40px;
  border-radius: 50%;
  font-size: 16px;
  color: var(--main-color);
  border: 1px solid var(--main-color);
  text-align: center;
  line-height: 38px;
  left: 0;
  top: 0;
}
.contact_info_item h3 {
  font-size: 18px;
  font-weight: 400;
  margin: 0 0 10px;
  color: var(--black-900);
}
.contact_info_item p {
  font-size: 16px;
  font-weight: 300;
  margin: 0;
  line-height: 26px;
  color: var(--black-400);
}
.contact .form-group {
  margin-bottom: 25px;
}
.contact .form-control {
  height: 52px;
  border: 1px solid transparent;
  box-shadow: var(--black-100);
  border-radius: 30px;
  padding: 0 24px;
  color: var(--black-900);
  background-color: var(--black-000);
  transition: 0.5s ease;
}
.contact .form-control:focus {
  border-color: var(--main-color);
}
.contact textarea.form-control {
  height: 140px;
  padding-top: 12px;
  resize: none;
}
</style>
