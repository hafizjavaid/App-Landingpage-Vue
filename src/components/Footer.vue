<template>
   
    <!-- -- Footer Start -->

    <footer class="footer">
      <div class="container">
        <div class="row">
          <div class="col-lg-3 col-md-6">
            <div class="footer-col">
              <h3>About us</h3>
              <p>
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nihil
                soluta magnam et, ipsum odio necessitatibus?
              </p>
            </div>
          </div>
          <div class="col-lg-3 col-md-6">
            <div class="footer-col">
              <h3>company</h3>
              <ul>
                <li><a href="#">privacy policy</a></li>
                <li><a href="#">terms & condition</a></li>

                <li><a href="#">latest blogs</a></li>

                <li><a href="#">app services</a></li>
              </ul>
            </div>
          </div>
          <div class="col-lg-3 col-md-6">
            <div class="footer-col">
              <h3>quick links</h3>
              <ul>
                <li><a href="#">privacy policy</a></li>
                <li><a href="#">terms & condition</a></li>

                <li><a href="#">latest blogs</a></li>

                <li><a href="#">app services</a></li>
              </ul>
            </div>
          </div>
          <div class="col-lg-3 col-md-6">
            <div class="footer-col">
              <h3>social pages</h3>
              <ul>
                <li><a href="#">privacy policy</a></li>
                <li><a href="#">terms & condition</a></li>

                <li><a href="#">latest blogs</a></li>

                <li><a href="#">app services</a></li>
              </ul>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-lg-12">
            <p class="copy">&copy; 2021 @ The Rigrex</p>
          </div>
        </div>
      </div>
    </footer>

    <!-- -- Footer Start -->
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

/* ============== Footer */
footer {
  background-color: var(--main-color);
  padding: 50px 0 0;
}
.footer-col h3 {
  font-size: 18px;
  font-weight: 500;
  color: #fff;
  margin: 0 0 25px;
  text-transform: capitalize;
}
.footer-col p {
  font-size: 16px;
  font-weight: 300;
  margin: 0;
  line-height: 26px;
  color: rgba(255, 255, 255, 0.9);
}
.footer-col ul {
  margin: 0;
}
.footer-col ul li:not(:last-child) {
  margin-bottom: 10px;
}
.footer-col ul li a {
  font-size: 16px;
  /* font-weight: 300; */
  color: rgba(255, 255, 255, 0.9);
  text-transform: capitalize;
  display: block;
  text-decoration: none;
  transition: 0.3s ease;
}
.footer-col ul li a:hover {
  padding-left: 5px;
}
footer .copy {
  margin-top: 50px !important;
  padding: 20px 0;
  text-align: center;
  font-size: 16px;
  font-weight: 300;
  margin: 0;
  color: rgba(255, 255, 255, 0.9);
  border-top: 1px solid rgba(255, 255, 255, 0.2);
}
</style>