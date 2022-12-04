<template>
  <div>
    <!-- Footer Style Seven Start -->
    <footer>
      <div class="container">
        <div class="section-content">
          <div class="row m-0">
            <div class="col-sm-4">
              <div class="footer-item footer-widget">
                <img
                  src="/assets/images/logo2.png"
                  alt="logoImage"
                  style="maxwidth: 90%"
                />
              </div>
            </div>

            <div class="col-sm-4">
              <div class="footer-item">
                <div class="footer-title">
                  <h5>Services</h5>
                </div>
                <a href="#" class="d-block">B2B Solutions</a>
                <a href="#" class="d-block">Accounting services</a>
                <a href="#" class="d-block">Networks & communications</a>
                <a href="#" class="d-block">Project management</a>
              </div>
            </div>

            <div class="col-sm-4">
              <div class="footer-item">
                <div class="footer-title">
                  <h5>Contact</h5>
                </div>
                <a href="#">
                  <i class="fa-solid fa-envelope"></i>
                  {{
                    $store.state.websiteSettings.find(
                      (one) => one.key === "email"
                    ).plain_value
                  }}
                </a>
                <a href="#">
                  <i class="fa-regular fa-clock"></i>
                  Mon – Fri: 10 am – 8 pm
                </a>
                <a href="#">
                  <i class="fa-solid fa-phone"></i>
                  (001) 234 56 78
                </a>
                <a href="#">
                  <i class="fa-solid fa-location-dot"></i>
                  New York, USA
                </a>
              </div>
            </div>
          </div>
          <div class="row m-0">
            <div class="col-12 copyrights">
              <p>© Powered By: Rail Coder – 2023. All rights reserved.</p>
            </div>
          </div>
        </div>
      </div>
    </footer>

    <!-- Footer Style Seven End -->
  </div>
</template>

<script>
export default {
  name: "AppFooter",
  components: {},
  data() {
    return {};
  },
  beforeMount() {},
  methods: {},
};
</script>
<style>
footer {
  padding: 90px 30px 0;
  background-color: #000000;
}
footer h5 {
  color: rgba(255, 255, 255, 0.5);
  font-size: 19px;
  font-weight: 600;
  line-height: 26.6px;
  margin-bottom: 30px;
}
footer .footer-item a {
  color: rgb(255, 255, 255);
  display: block;
  font-size: 15px;
  font-weight: 400;
  line-height: 22.5px;
  text-align: left;
  text-decoration: none;
  margin-bottom: 15px;
}
footer .footer-item a:hover {
  color: var(--main-color);
}
footer .footer-item a i {
  color: var(--main-color);
  margin-right: 10px;
}
footer .copyrights p {
  color: rgba(255, 255, 255, 0.5);
  font-size: 13px;
  font-weight: 400;
  line-height: 18.2px;
  text-align: left;
  padding: 90px 0 30px;
}
</style>
