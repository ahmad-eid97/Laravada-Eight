<template>
  <div class="home">
        <!-- Slick Section Start -->
        <app-home-slider></app-home-slider>
        <!-- Slick Section End -->
        
        <app-home-feature></app-home-feature>

        <app-home-services></app-home-services>
        <app-home-contact-divider></app-home-contact-divider>
        <app-home-principles></app-home-principles>
        <app-home-cases></app-home-cases>
        <app-home-achievements></app-home-achievements>
        <app-home-why></app-home-why>
        <app-home-blogs></app-home-blogs>
        <app-home-contact-divider-bottom></app-home-contact-divider-bottom>
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
import AppHomeAchievements from '../components/home/AppHomeAchievements.vue'
import AppHomeBlogs from '../components/home/AppHomeBlogs.vue'
import AppHomeCases from '../components/home/AppHomeCases.vue'
import AppHomeContactDivider from '../components/home/AppHomeContactDivider.vue'
import AppHomeContactDividerBottom from '../components/home/AppHomeContactDividerBottom.vue'
import AppHomeFeature from '../components/home/AppHomeFeature.vue'
// import AppHomeNews from '../components/home/AppHomeNews.vue'
import AppHomePrinciples from '../components/home/AppHomePrinciples.vue'
import AppHomeServices from '../components/home/AppHomeServices.vue'
// import AppHomeServicesOffers from '../components/home/AppHomeServicesOffers.vue'
import AppHomeSlider from '../components/home/AppHomeSlider.vue'
// import AppHomeTestimonials from '../components/home/AppHomeTestimonials.vue'
import AppHomeWhy from '../components/home/AppHomeWhy.vue'
// @ is an alias to /src


export default {
  name: 'Home',
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
    AppHomeContactDividerBottom
  }
}
</script>
