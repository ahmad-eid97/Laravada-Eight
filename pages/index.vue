<template>
  <div class="home">
    <!-- Slick Section Start -->
    <app-home-slider :slides="slides"></app-home-slider>
    <!-- Slick Section End -->

    <app-home-feature :features="features"></app-home-feature>

    <app-home-services :services="services"></app-home-services>
    <app-home-contact-divider></app-home-contact-divider>
    <app-home-principles></app-home-principles>
    <app-home-cases :activities="activities"></app-home-cases>
    <app-home-achievements :counter="counter"></app-home-achievements>
    <app-home-why :whyUs="whyUs" :team="team"></app-home-why>
    <app-home-steps :steps="steps" />
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
    <app-home-partners :partners="partners" />
    <SocialChat :attendants="attendants">
      <p slot="header">Click one of our representatives below to chat.</p>
      <template v-slot:button="{ open }">
        <span v-show="!open">Contact us</span>
        <span v-show="open">Close</span>
      </template>
      <small slot="footer">Opening hours: 8am to 10pm</small>
    </SocialChat>
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
import AppHomeSteps from "../components/home/AppHomeSteps.vue";
import AppHomePartners from "../components/home/AppHomePartners.vue";
// @ is an alias to /src

export default {
  name: "Home",
  data() {
    return {
      attendants: [
        {
          app: "whatsapp",
          label: "Support",

          name: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_whatsapp_label"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_whatsapp_label"
              ).plain_value
            : "Laravada",

          number: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_whatsapp_number"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_whatsapp_number"
              ).plain_value
            : "11111111111",

          avatar: {
            src: "https://avatars0.githubusercontent.com/u/8084606?s=460&u=20b6499a416cf7129a18e5c168cf387e159edb1a&v=4",
            alt: "Laravada customer support",
          },
        },
        {
          app: "messenger",
          label: "Technical support",

          name: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_messenger_label"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_messenger_label"
              ).plain_value
            : "Laravada Facebook",

          id: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_messenger_id"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_messenger_id"
              ).plain_value
            : "111111111111",

          avatar: {
            src: "https://avatars0.githubusercontent.com/u/8084606?s=460&u=20b6499a416cf7129a18e5c168cf387e159edb1a&v=4",
            alt: "Laravada customer support",
          },
        },
      ],
    };
  },
  async asyncData({ $axios, app }) {
    const slides = await $axios.get("/sliders", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

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

    const activities = await $axios.get("/sections/activities", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const steps = await $axios.get("/sections/steps", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const partners = await $axios.get("/partners");

    return {
      slides: slides.data.data.sliders,
      features: features.data.data,
      partners: partners.data.data.partners,
      counter: counter.data.data,
      whyUs: whyUs.data.data,
      services: services.data.data.services,
      blogs: blogs.data.data.blogs,
      bottomBanner: bottomBanner.data.data,
      team: TEAM.data.data.teams.slice(0, 1),
      activities: activities.data.data,
      steps: steps.data.data,
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
    AppHomeSteps,
    AppHomePartners,
  },
};
</script>

<style lang="scss">
.home {
  --vsc-bg-header: var(--main-color);
  --vsc-bg-footer: var(--main-color);
  --vsc-text-color-header: #fff;
  --vsc-text-color-footer: #fff;
  --vsc-bg-button: var(--main-color);
  --vsc-text-color-button: #fff;
  --vsc-outline-color: var(--main-color);
  --vsc-border-color-bottom-header: #fff;
  --vsc-border-color-top-footer: #fff;
}
</style>
