<template>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg fixed-top">
    <div class="container">
      <!-- Brand -->
      <a href="index.html" class="navbar-brand">Rigrex app</a>
      <!-- Toggler -->
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#myNav"
      >
        <i class="fas fa-bars"></i>
      </button>

      <!-- Nav Links -->
      <div class="collapse navbar-collapse" id="myNav">
        <ul class="navbar-nav ml-auto">
          <li v-for="link in links" :key="link.text" :class="link.class1">
            <a href="" :class="link.class2">{{ link.text }}</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <!-- Navbar -->
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          class1: "nav-item",
          class2: "nav-link",
          text: "Home",
        },
        {
          class1: "nav-item",
          class2: "nav-link",
          text: "Fetaures",
        },
        {
          class1: "nav-item",
          class2: "nav-link",
          text: "Screenshots",
        },
        {
          class1: "nav-item",
          class2: "nav-link",
          text: "Team",
        },
        {
          class1: "nav-item",
          class2: "nav-link",
          text: "Pricing",
        },
        {
          class1: "nav-item",
          class2: "nav-link",
          text: "Contact",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
/* ------------- Navbar */
nav {
  background-color: var(--main-color);
  background-color: transparent;

  padding: 20px 0;
  transition: all 0.5s ease;
}
nav.navbar_shrink {
  box-shadow: 0 10px 10px rgba(0, 0, 0, 0.1);
  background-color: var(--main-color);
  padding: 10px 0;
}
nav > .container {
  padding: 0 15px;
}
nav .navbar-brand {
  font-size: 30px;
  color: #fff;
  font-weight: 500;
  text-transform: capitalize;
}
nav .nav-item {
  margin-left: 40px;
}

nav .nav-item .nav-link {
  color: #fff;
  /* text-transform: uppercase;
     */
  font-size: 16px;
  font-weight: 400;
  padding: 5px 0;
  position: relative;
}
nav .nav-item .nav-link::before {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  right: 0;
  height: 1px;
  background-color: #fff;
  transition: 0.5s ease;
  transform: scale(0);
}
nav .nav-item .nav-link:hover:before,
nav .nav-item .nav-link.active:before {
  transform: scale(1);
}

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
}
/* ------------- Navbar */
</style>
