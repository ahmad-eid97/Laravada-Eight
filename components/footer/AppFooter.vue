<template>
  <div>
    <!-- Footer Style Seven Start -->
    <subscribe />
    <footer>
      <div class="container">
        <div class="section-content">
          <div class="row m-0">
            <div class="col-sm-4">
              <div class="footer-item footer-widget">
                <img
                  :src="
                    $store.state.websiteSettings.find(
                      (one) => one.key === 'logo'
                    ).plain_value
                  "
                  alt="logoImage"
                  style="width: 200px"
                />
                <p>
                  {{
                    $store.state.websiteSettings.find(
                      (one) => one.key === "description"
                    ).plain_value
                  }}
                </p>
              </div>
            </div>

            <div class="col-sm-4">
              <div class="footer-item">
                <h5>OTHER PAGES</h5>
                <ul class="footer-list">
                  <!-- <li><a href="#">About Us</a></li> -->
                  <li v-for="page in $store.state.footerPages" :key="page.id">
                    <b-nav-item
                      :to="localePath(generatePagePath(page.id))"
                      v-if="page.status"
                      >{{ page.name }}</b-nav-item
                    >
                  </li>
                </ul>
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
                  <i class="fa-solid fa-phone"></i>

                  {{
                    $store.state.websiteSettings.find(
                      (one) => one.key === "contact_phone"
                    ).plain_value
                  }}
                </a>
                <a href="#">
                  <i class="fa-solid fa-location-dot"></i>
                  {{
                    $store.state.websiteSettings.find(
                      (one) => one.key === "contact_address"
                    ).plain_value
                  }}
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
import Subscribe from "../subscribe/subscribe.vue";
export default {
  name: "AppFooter",
  components: { Subscribe },
  data() {
    return {};
  },
  beforeMount() {},
  methods: {
    generatePagePath(id) {
      switch (id) {
        case 1:
          return "/about";
        case 2:
          return "/contact";
        case 3:
          return "/terms";
        case 4:
          return "/policy";
      }
    },
  },
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
