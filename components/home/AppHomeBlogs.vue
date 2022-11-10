<template>
  <section class="blogs">
        <div class="row">
            <h2>From our blog</h2>
        </div>
        <div class="row">
            <swiper :options="swiperOption">
                <swiper-slide>
                    <div class="item">
                        <div class="image">
                            <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-0-1.jpg" alt="">
                        </div>
                        <h5><a href="#">Amet tincidunt elit habitant morbi tristique</a></h5>
                        <p>
                            <span><a href="#">Company</a>,<a href="#">Technology</a></span>
                            <span><a href="#"> - 5 February 2020</a></span>
                        </p>
                        <a href="#" class="btn">Read article</a>
                    </div>
                </swiper-slide>

                <swiper-slide>
                    <div class="item">
                        <div class="image">
                            <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-1-1.jpg" alt="">
                        </div>
                        <h5><a href="#">Maecenas sit – amet tincidunt habitant morbi dolor</a></h5>
                        <p>
                            <span><a href="#">Company</a></span>
                            <span><a href="#"> - 5 February 2020</a></span>
                        </p>
                        <a href="#" class="btn">Read article</a>
                    </div>
                </swiper-slide>

                <swiper-slide>
                    <div class="item">
                        <div class="image">
                            <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-2-1.jpg" alt="">
                        </div>
                        <h5><a href="#">Nunc ut – for dictum purus lorem malesuada famesla</a></h5>
                        <p>
                            <span><a href="#">Business</a></span>
                            <span><a href="#"> - 5 February 2020</a></span>
                        </p>
                        <a href="#" class="btn">Read article</a>
                    </div>
                </swiper-slide>

                <swiper-slide>
                    <div class="item">
                        <div class="image">
                            <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-5-1.jpg" alt="">
                        </div>
                        <h5><a href="#">Pellen lorem: tesque habitant morbi tristique</a></h5>
                        <p>
                            <span><a href="#">Technology</a></span>
                            <span><a href="#"> - 5 February 2020</a></span>
                        </p>
                        <a href="#" class="btn">Read article</a>
                    </div>
                </swiper-slide>

                <swiper-slide>
                    <div class="item">
                        <div class="image">
                            <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/01/img001-8-1.jpg" alt="">
                        </div>
                        <h5><a href="#">Pellentesque habitant morbi tristique</a></h5>
                        <p>
                            <span><a href="#">Company</a></span>
                            <span><a href="#"> - 24 August 2019</a></span>
                        </p>
                        <a href="#" class="btn">Read article</a>
                    </div>
                </swiper-slide>

                <swiper-slide>
                    <div class="item">
                        <div class="image">
                            <img class="img-fluid" src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-9-1.jpg" alt="">
                        </div>
                        <h5><a href="#">Netus et malesuada – fames nulla from ac turpis egestas</a></h5>
                        <p>
                            <span><a href="#">Business</a>,<a href="#">Technology</a></span>
                            <span><a href="#"> - 5 May 2018</a></span>
                        </p>
                        <a href="#" class="btn">Read article</a>
                    </div>
                </swiper-slide>
            </swiper>
        </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomeBlogs',
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
    .blogs {
        padding: 90px 30px;
    }
    .blogs h2 {
        color: rgb(34, 34, 34);
        font-size: 36px;
        font-weight: 600;
        line-height: 43.2px;
        padding: 0 30px 30px;
        text-align: center;
    }
    .blogs .slick-slide  {
        text-align: center;
    }
    .blogs .item {
        max-width: 360px;
        text-align: center;
        margin: auto;
    }
    
    .blogs .item .image {
        max-height: 237.6px;
        position: relative;
        margin-bottom: 30px;
    }
    .blogs .item .image:after {
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
    .blogs .item .image:hover::after {
        opacity: 0.9;
    }
    .blogs .item h5 {
        text-align: center;
    }
    .blogs .item h5 a{
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
    .blogs .item h5 a:hover{
        color: rgb(48, 164, 108);
    }
    .blogs .item p a{
        color: rgb(153, 153, 153);
        display: inline-block;
        font-family: "Mulish", sans-serif;
        font-size: 13px;
        font-weight: 400;
        line-height: 18.2px;
        text-decoration-color: rgb(153, 153, 153);
        text-decoration: none;
    }
    .blogs .item .btn {
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
    .blogs .item .btn:hover {
       background-color: rgb(40, 134, 89);
    }
    .blogs .slick-prev {
        left: -5px;
        z-index: 1;
        width: 40px;
    }
    .blogs .slick-next {
        right: -5px;
        z-index: 1;
        width: 40px;
    }
    .blogs .slick-prev::before, .blogs .slick-next::before {
        font-size: 30px;
        color: #000;
    }
</style>