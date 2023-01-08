<template>
  <section class="slider-wrapper intro p-0">
    <VueSlickCarousel
      :fade="true"
      :arrows="true"
      :slidesToShow="1"
      :focusOnSelect="true"
      :dots="false"
    >
      <div
        class="item item-1"
        v-for="slide in slides"
        :key="slide.id"
        :style="{ background: `url(${slide.background})` }"
      >
        <div class="overlay"></div>
        <div class="content">
          <h1>
            {{ slide.title }}
          </h1>
          <p>
            {{ slide.description }}
          </p>
          <a :href="slide.link" class="btn">Learn More</a>
        </div>
      </div>
    </VueSlickCarousel>
  </section>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

export default {
  name: "AppHomeSlider",
  components: { VueSlickCarousel },
  props: ["slides"],
  data() {
    return {
      c1: undefined,
      c2: undefined,
    };
  },
  methods: {},
  mounted() {
    this.c1 = this.$refs.c1;
    this.c2 = this.$refs.c2;
  },
};
</script>
<style lang="scss">
.intro .slick-slide .item {
  min-height: 100vh;
  position: relative;
}
.intro .slick-slide .item {
  /* background-image: url(//the7.io/elementor-business/wp-content/uploads/sites/89/2020/01/img001-8-1.jpg\\); */
  background-size: cover;
  background-position: 0;
}
.intro .slick-slide .item .overlay {
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  background-image: linear-gradient(
    180deg,
    rgba(0, 0, 0, 0.5) 90%,
    rgb(250, 250, 250) 100%
  );
  z-index: 0;
}
.intro .slick-slide .item .content {
  z-index: 1;
  position: relative;
  padding: 200px 60px 90px;
}
.intro .slick-slide .item .content h1 {
  color: rgb(255, 255, 255);
  text-align: left;
  line-height: 64px;
  letter-spacing: 0px;
  font-weight: 700;
  font-size: 56px;
  opacity: 1;
  position: relative;
}
.intro .slick-slide .item .content h1:after {
  content: "";
  height: 4px;
  position: absolute;
  bottom: -30px;
  left: 0;
  width: 50%;
  background-color: var(--main-color);
}
.intro .slick-slide .item .content p {
  color: rgb(255, 255, 255);
  text-align: left;
  line-height: 36px;
  letter-spacing: 0px;
  font-weight: 400;
  font-size: 24px;
  margin-top: 55px;
  max-width: 660px;
}
@include xs {
  .intro .slick-slide .item .content h1 {
    line-height: 44px;
    font-size: 36px;
  }
  .intro .slick-slide .item .content p {
    line-height: 36px;
    font-size: 18px;
  }
}
.intro .slick-slide .item .content .btn {
  background-color: rgb(48, 164, 108);
  border-radius: 3px;
  color: rgb(255, 255, 255);
  cursor: pointer;
  display: inline-block;
  font-size: 17px;
  font-weight: 600;
  height: 47px;
  line-height: 17px;
  padding-bottom: 15px;
  padding-top: 15px;
  border: none;
  min-width: 170px;
}
.intro .slick-slide .item .content .btn:hover {
  background-color: rgb(40, 134, 89);
}
.intro .slick-prev {
  left: 5px;
  z-index: 1;
  width: 40px;
}
.intro .slick-next {
  right: 5px;
  z-index: 1;
  width: 40px;
}
.intro .slick-prev::before,
.intro .slick-next::before {
  /* font-size: 40px; */
}
</style>
