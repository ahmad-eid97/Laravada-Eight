<template>
  <section class="cases">
        <div class="row">
            <h2>Featured cases</h2>
        </div>
        <div class="row">
            <swiper :options="swiperOption">
                <swiper-slide>
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-46-1.jpg" alt="">
                    </div>
                    <h5><a href="#">Amet from ipsum</a></h5>
                    <p>
                        Morbi dapibus a tellus - at aecenas sit amet tincidunt elit dolor senec euismod lorem ipsum dolor.
                    </p>
                    <a href="#" class="btn">View case</a>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/01/img001-8-1.jpg" alt="">
                    </div>
                    <h5><a href="#">Ipsum from dolor amet</a></h5>
                    <p>
                        Dolor proin eget ex convallis eu viverra lorem pretium habitant morbi tristique senec.
                    </p>
                    <a href="#" class="btn">View case</a>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-1-1.jpg" alt="">
                    </div>
                    <h5><a href="#">Nulla glavrida</a></h5>
                    <p>
                        Ex convallis eu viverra lorem pretium tellus dolor amet at euismod.
                    </p>
                    <a href="#" class="btn">View case</a>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-41-1.jpg" alt="">
                    </div>
                    <h5><a href="#">Morbi dapibus</a></h5>
                    <p>
                        Convallis eu viverra lorem pretium. Morbi dapibus a tellus at euismod.
                    </p>
                    <a href="#" class="btn">View case</a>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-45-1.jpg" alt="">
                    </div>
                    <h5><a href="#">Class aptent taciti</a></h5>
                    <p>
                        Class aptent taciti sociosqu ad litora torquent per conus.
                    </p>
                    <a href="#" class="btn">View case</a>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-3-1.jpg" alt="">
                    </div>
                    <h5><a href="#">Lorem ipsum dolor</a></h5>
                    <p>
                        Ut sit amet semper arcu – dolor proin eget ex convallis eu viverra lorem pretium. 
                    </p>
                    <a href="#" class="btn">View case</a>
                </div>
                </swiper-slide>
            </swiper>
        </div>
  </section>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'; 
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
    name: 'AppHomeCases',
    components: {VueSlickCarousel},
    data() {
        return {
      swiperOption: {
        loop: true,
        slidesPerView: 3,
        spaceBetween: 50,
        breakpoints: {
          // when window width is >= 320px
          100: {
            slidesPerView: 1,
            spaceBetween: 5,
          },
          // when window width is >= 480px
          480: {
            slidesPerView: 1,
            spaceBetween: 5,
          },
          // when window width is >= 640px
          640: {
            slidesPerView: 2,
            spaceBetween: 5,
          },
          992: {
            slidesPerView: 3,
            spaceBetween: 5,
          },
          1200: {
            slidesPerView: 3,
            spaceBetween: 5,
          },
        },
      },

        }
    }

}
</script>

<style>
    .cases {
        padding: 90px 30px;
    }
    .cases h2 {
        color: rgb(34, 34, 34);
        font-size: 36px;
        font-weight: 600;
        line-height: 43.2px;
        padding: 0 30px 30px;
        text-align: center;
    }
    .cases .slick-slide  {
        text-align: center; 
    }
    .cases .item {
        max-width: 360px;
        text-align: center;
        margin: auto;
    }
    
    .cases .item .image {
        max-height: 237.6px;
        position: relative;
        margin-bottom: 30px;
    }
    .cases .item .image:after {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        z-index: 1;
        background-image: linear-gradient(rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 0.5) 100%);
        opacity: 0;
        transition: all 0.3s linear;
    }
    .cases .item .image:hover::after {
        opacity: 0.9;
    }
    .cases .item h5 {
        text-align: center;
    }
    .cases .item h5 a{
        color: rgb(34, 34, 34);
        font-size: 19px;
        font-weight: 600;
        line-height: 26.6px;
        text-decoration-color: rgb(34, 34, 34);
        text-decoration-line: none;
        text-decoration-style: solid;
        transition-delay: 0s;
        transition-duration: 0.3s;
        transition-property: all;
        transition-timing-function: ease;
        word-spacing: 0px;
    }
    .cases .item h5 a:hover{
        color: rgb(48, 164, 108);
    }
    .cases .item p{
        color: rgb(102, 102, 102);
        font-size: 17px;
        font-weight: 400;
        line-height: 27.2px;
        margin-top: 10px;
        text-align: center;
        transition-delay: 0s;
        transition-duration: 0.3s;
        transition-property: all;
        transition-timing-function: ease;
    }
    .cases .item .btn {
        background-color: rgb(48, 164, 108);
        border-radius: 3px;
        color: rgb(255, 255, 255);
        cursor: pointer;
        display: inline-block;
        font-size: 12px;
        font-weight: 600;
        line-height: 17px;
        padding: 6px 14px;
        border: none;
        min-width: 80px;
    }
    .cases .item .btn:hover {
       background-color: rgb(40, 134, 89);
    }
    .cases .slick-prev {
        left: -5px;
        z-index: 1;
        width: 40px;
    }
    .cases .slick-next {
        right: -5px;
        z-index: 1;
        width: 40px;
    }
    .cases .slick-prev::before, .cases .slick-next::before {
        font-size: 30px;
        color: #000;
    }
</style>