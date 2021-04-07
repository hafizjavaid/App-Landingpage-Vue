<template>
  <div id="app">
    <Navbar></Navbar>
    <Banner></Banner>
    <Features></Features>
    <Funfacts></Funfacts>
    <Appsc></Appsc>
    <Download></Download>
    <Work></Work>
    <Review></Review>
    <Price></Price>
    <Team></Team>
    <Contact></Contact>
    <Footer></Footer>
  </div>
</template>
<script>
import Navbar from "./components/Navbar";
import Banner from "./components/Banner";
import Features from "./components/Features";
import Funfacts from "./components/Funfacts"
import Appsc from "./components/Appsc"
import Download from "./components/Download"
import Work from "./components/Work"
import Review from "./components/Review"
import Price from "./components/Price"
import Team from "./components/Team"
import Contact from "./components/Contact"
import Footer from "./components/Footer"
export default {
  components: {
    Navbar,
    Banner,
    Features,
    Funfacts,
    Appsc,
    Download,
    Work,
    Review,
    Price,
    Team,
    Contact,
    Footer
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap");
:root {
  --main-color: #8280fb;
  --color-1: #e91e63;
  --color-2: #f5ae10;
  --color-3: #09d69c;
  --bg-dark: #2b2c2f;
  --main-to-dark-color: var(--main-color);
  --dark-to-main-color: var(--bg-dark);
  --shadow-100: 0 5px 15px rgba(0, 0, 0, 0.1);
  --shadow-300: 0 5px 15px rgba(0, 0, 0, 0.3);
  --black-900: #000;
  --black-400: #555;
  --black-100: #f7f7f7;
  --black-000: #fff;
  --black-alpha-100: rgba(0, 0, 0, 0.05);
}
* {
  margin: 0;
  padding: 0;
  outline: none !important;
  box-sizing: border-box;
  font-family: sans-serif;
  font-family: "Poppins", sans-serif;
}
body {
  font-size: 16px;
  font-weight: 400;
  overflow-x: hidden;
  background-color: #fff;
  line-height: 1.5;
  --main-color: #8280fb;
  --color-1: #e91e63;
  --color-2: #f5ae10;
  --color-3: #09d69c;
  --bg-dark: #2b2c2f;
  --main-to-dark-color: var(--main-color);
  --dark-to-main-color: var(--bg-dark);
  --shadow-100: 0 5px 15px rgba(0, 0, 0, 0.1);
  --shadow-300: 0 5px 15px rgba(0, 0, 0, 0.3);
  --black-900: #000;
  --black-400: #555;
  --black-100: #f7f7f7;
  --black-000: #fff;
  --black-alpha-100: rgba(0, 0, 0, 0.05);
}
body.dark {
  background-color: var(--bg-dark);
  --black-100: var(--bg-dark);
  --black-000: var(--bg-dark);
  --main-to-dark-color: var(--bg-dark);
  --dark-to-main-color: var(--main-color);
  --black-900: #fff;
  --black-400: #bbb;
  --shadow-100: var(--shadow-300);
  --black-alpha-100: rgba(255, 255, 255, 0.05);
}
img {
  max-width: 100%;
  vertical-align: middle;
}
ul {
  list-style: none;
}
.btn-1 {
  background-color: #fff;
  padding: 12px 30px;
  border: none;
  border-radius: 30px;
  color: var(--main-color);
  text-transform: capitalize;
  transition: 0.5s ease;
  box-shadow: var(--shadow-300);
  font-weight: 500;
}
.btn-1:focus {
  box-shadow: var(--shadow-300);
}
.btn-1:hover {
  color: #fff;
  background-color: var(--main-color);
}

.btn-2 {
  background-color: var(--main-color);
  padding: 12px 30px;
  border: none;
  border-radius: 30px;
  color: #fff;
  text-transform: capitalize;
  transition: 0.5s ease;
  box-shadow: var(--shadow-100);
  font-weight: 500;
}
.btn-2:focus {
  box-shadow: var(--shadow-100);
}
.btn-2:hover {
  color: var(--main-color);
  background-color: #fff;
}
@keyframes spin_01 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@keyframes bounceTop_01 {
  0%,
  100% {
    transform: translateY(-30px);
  }
  50% {
    transform: translateY(0px);
  }
}
@keyframes pulse_01 {
  0% {
    transform: scale(0.94);
    box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.7);
  }
  70% {
    transform: scale(1);
    box-shadow: 0 0 0 12px rgba(255, 255, 255, 0);
  }
  100% {
    transform: scale(0.94);
    box-shadow: 0 0 0 0 rgba(255, 255, 255, 0);
  }
}
.effect_wrap .effect {
  position: absolute;
  z-index: -1;
}
.effect_wrap .effect_1 {
  left: 20%;
  top: 20%;
  font-size: 20px;
  color: var(--color-2);
  animation: spin_01 5s linear infinite;
}
.effect_wrap .effect_2 {
  right: 5%;
  top: 10%;
  font-size: 25px;
  color: var(--color-2);
  color: rgba(255, 255, 255, 0.7);
  animation: spin_01 7s linear infinite;
}
.effect_wrap .effect_3 {
  left: 5%;
  bottom: 30%;
  font-size: 25px;
  color: var(--color-3);
  animation: bounceTop_01 3s linear infinite;
}

.section_padding {
  padding: 80px 0;
}
.section_title h2 {
  font-size: 40px;
  color: var(--black-900);

  font-weight: 700;
  text-transform: capitalize;
  text-align: center;
  margin: 0;
}
.section_title {
  margin-bottom: 40px;
}
.section_title h2 span {
  color: var(--main-color);
}

/* =================== Responsiveness */
@media (max-width: 991px) {
  .navbar-toggler {
    background-color: var(--dark-to-main-color);
    box-shadow: var(--shadow-300);
    height: 34px;
    width: 44px;
    padding: 0;
    font-size: 17px;
    color: #fff;
  }
  .navbar-nav {
    background-color: var(--dark-to-main-color);
    box-shadow: var(--shadow-300);
  }
  .navbar .nav-item {
    margin: 0;
    padding: 5px 15px;
  }
  .navbar.navbar_shrink .navbar-toggler,
  .navbar.navbar_shrink .navbar-nav {
    background-color: var(--main-color);
  }
  .home-img .circle {
    height: 320px;
    width: 320px;
  }
  .home-img .circle::before {
    left: 18px;
    top: 18px;
    transform-origin: 142px 142px;
  }
  .home-text h1 {
    font-size: 40px;
  }
  .app_download_item,
  .h_works_item,
  .pricing_plan {
    margin-bottom: 30px;
  }
  .h_works_item.line_right::before {
    content: none;
  }
  .h_works_item {
    box-shadow: var(--shadow-100);
    border-radius: 10px;
  }
  .footer-col {
    margin-bottom: 30px;
  }
}

@media (max-width: 767px) {
  .home-text {
    margin-bottom: 80px;
  }
  .fun_facts_img {
    margin-bottom: 30px;
  }
  form {
    margin-top: 20px;
  }
  .section_title h2 {
    font-size: 35px;
  }
  .fun_facts .section_title h2 {
    text-align: center;
  }
}
@media (max-width: 575px) {
  .home-text h1 {
    font-size: 30px;
  }
  .home-text p {
    font-size: 16px;
  }
  .section_title h2 {
    font-size: 32px;
  }
}
/* =================== Responsiveness */
</style>
