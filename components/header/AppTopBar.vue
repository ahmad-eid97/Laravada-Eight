<template>
  <div class="top-bar">
    <div class="row m-0">
      <div class="col-lg-12">
        <ul class="social-icon bordered-theme">
          <li>
            <span class="tel"> tel. +1111111111 </span>
          </li>
          <li>
            <a href="#">
              <i class="fa-brands fa-facebook-f"></i>
            </a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-twitter"></i> </a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-linkedin-in"></i> </a>
          </li>
          <li>
            <a href="#"><i class="fa-solid fa-wifi"></i> </a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-youtube"></i> </a>
          </li>
          <lang-switch></lang-switch>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import LangSwitch from "../langSwitch/langSwitch.vue";
export default {
  name: "AppTopBar",
  components: {
    LangSwitch,
  },
  data() {
    return {};
  },
  mounted() {},
  methods: {},
};
</script>
<style>
.top-bar {
  padding: 20px 60px 0;
  height: 60px;
  transition: all 0.3s linear;
}
.top-bar .social-icon {
  list-style: none;
  padding: 0;
  display: flex;
  justify-content: end;
}
.top-bar .social-icon li {
  display: inline-block;
  margin-left: 6px;
}
.top-bar .social-icon li .tel {
  margin-right: 10px;
  color: rgb(255, 255, 255);
  font-size: 13px;
  font-weight: 400;
  line-height: 18.2px;
}
.top-bar .social-icon li a {
  display: block;
  background-color: rgb(48, 164, 108);
  border-radius: 3px;
  font-size: 11px;
  line-height: 13px;
  padding: 5px;
  text-align: center;
  text-decoration-color: rgb(129, 138, 145);
  text-decoration-style: solid;
  color: #fff;
  width: 24px;
  height: 24px;
}
</style>
