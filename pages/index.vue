<template>
  <div class="home">
    <!-- Slick Section Start -->
    <app-home-slider :sliderData="sliderData"></app-home-slider>
    <!-- Slick Section End -->

    <app-home-feature :features="features"></app-home-feature>

    <app-home-services :services="services"></app-home-services>
    <app-home-contact-divider></app-home-contact-divider>
    <app-home-principles></app-home-principles>
    <app-home-cases></app-home-cases>
    <app-home-achievements :counter="counter"></app-home-achievements>
    <app-home-why :whyUs="whyUs" :team="team"></app-home-why>
    <app-home-blogs :blogs="blogs"></app-home-blogs>
    <app-home-contact-divider-bottom
      :bottomBanner="bottomBanner"
    ></app-home-contact-divider-bottom>
    <!-- <app-home-testimonials></app-home-testimonials> -->

    <!-- WHY WORK WITH US Start -->
    <!-- WHY WORK WITH US End -->

    <!-- testimonials Section Start -->
    <!-- testimonials Section End -->

    <!-- <app-home-news></app-home-news> -->

    <!-- Services Section Start -->
    <!-- <app-home-services-offers></app-home-services-offers> -->
  </div>
</template>

<script>
import AppHomeAchievements from "../components/home/AppHomeAchievements.vue";
import AppHomeBlogs from "../components/home/AppHomeBlogs.vue";
import AppHomeCases from "../components/home/AppHomeCases.vue";
import AppHomeContactDivider from "../components/home/AppHomeContactDivider.vue";
import AppHomeContactDividerBottom from "../components/home/AppHomeContactDividerBottom.vue";
import AppHomeFeature from "../components/home/AppHomeFeature.vue";
// import AppHomeNews from '../components/home/AppHomeNews.vue'
import AppHomePrinciples from "../components/home/AppHomePrinciples.vue";
import AppHomeServices from "../components/home/AppHomeServices.vue";
// import AppHomeServicesOffers from '../components/home/AppHomeServicesOffers.vue'
import AppHomeSlider from "../components/home/AppHomeSlider.vue";
// import AppHomeTestimonials from '../components/home/AppHomeTestimonials.vue'
import AppHomeWhy from "../components/home/AppHomeWhy.vue";
// @ is an alias to /src

export default {
  name: "Home",
  async asyncData({ $axios, app }) {
    const sliderData = await $axios.get("/sliders");

    const features = await $axios.get("/sections/features", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const counter = await $axios.get("/sections/counter_success", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const whyUs = await $axios.get("/sections/why_choose_us", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const services = await $axios.get("/services");

    const blogs = await $axios.get("/blogs?latest=1");

    const bottomBanner = await $axios.get("/sections/banner-bottom", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const TEAM = await $axios.get("/teams");

    return {
      sliderData: sliderData.data.data.sliders,
      features: features.data.data,
      counter: counter.data.data,
      whyUs: whyUs.data.data,
      services: services.data.data.services,
      blogs: blogs.data.data.blogs,
      bottomBanner: bottomBanner.data.data,
      team: TEAM.data.data.teams.slice(0, 1),
    };
  },
  components: {
    AppHomeSlider,
    AppHomeFeature,
    AppHomeBlogs,
    AppHomeContactDivider,
    AppHomeWhy,
    AppHomeServices,
    // AppHomeTestimonials,
    // AppHomeNews,
    // AppHomeServicesOffers,
    AppHomePrinciples,
    AppHomeCases,
    AppHomeAchievements,
    AppHomeContactDividerBottom,
  },
};
</script>
