<template>
    <section class="slider-wrapper intro p-0">
        <VueSlickCarousel :fade="true" :arrows="true" :slidesToShow="1" :focusOnSelect="true" :dots="false" >
            <div class="item item-1">
                <div class="overlay"></div>
                <div class="content">
                    <h1>Networks & Communications</h1>
                    <p>
                        Class aptent litora torquent per inceptos himenaeos - tellus at euismod lorem ipsum dolor. Morbi dapibus glavrida ipsum dolor at euismod amet.
                    </p>
                    <a href="#" class="btn">
                        View details
                    </a>
                </div>
            </div>
            <div class="item item-2">
                <div class="overlay"></div>
                <div class="content">
                    <h1>Accounting Services</h1>
                    <p>
                        Ut sit amet semper arcu? Proin eget ex viverra lorem pretium. Morbi dapibus a tellus at euismod. Ut dolor amet sit amet semper!
                    </p>
                    <a href="#" class="btn">
                        View details
                    </a>
                </div>
            </div>
            <div class="item item-3">
                <div class="overlay"></div>
                <div class="content">
                    <h1>Project Management</h1>
                    <p>
                        Class aptent litora torquent per inceptos himenaeos - tellus at euismod lorem ipsum dolor. Morbi dapibus glavrida ipsum dolor at euismod amet.
                    </p>
                    <a href="#" class="btn">
                        View details
                    </a>
                </div>
            </div>
            <div class="item item-4">
                <div class="overlay"></div>
                <div class="content">
                    <h1>B2B Solutions</h1>
                    <p>
                        Etiam mollis libero vitae pulvinar bibendum. Morbi convallis metus eros, semper pharetra massa efficitur auctor nulla amet ipsum.
                    </p>
                    <a href="#" class="btn">
                        View details
                    </a>
                </div>
            </div>
        </VueSlickCarousel>
    </section>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
 import 'vue-slick-carousel/dist/vue-slick-carousel.css'; 
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

export default {
    name: 'AppHomeSlider',
    components: {VueSlickCarousel},
    data() {
        return {
            c1: undefined,
            c2: undefined,
        }
    },
    methods : {
        
    },
    mounted() {
        this.c1 = this.$refs.c1;
        this.c2 = this.$refs.c2;
    },
}
</script>
<style lang="scss">
    .intro .slick-slide .item {
        min-height: 100vh;
        position: relative;
    }
    .intro .slick-slide .item-1 {
        background-image: url(//the7.io/elementor-business/wp-content/uploads/sites/89/2020/01/img001-8-1.jpg\\);
        background-size: cover;
        background-position: 0;
    }
    .intro .slick-slide .item-2 {
        background-image: url(//the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-1-1.jpg);
        background-size: cover;
        background-position: 0;
    }
    .intro .slick-slide .item-3 {
        background-image: url(//the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-6-1.jpg);
        background-size: cover;
        background-position: 0;
    }
    .intro .slick-slide .item-4 {
        background-image: url(//the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-25-1.jpg);
        background-size: cover;
        background-position: 0;
    }
    .intro .slick-slide .item .overlay {
        position: absolute;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-image: linear-gradient(180deg, rgba(0, 0, 0, 0.5) 90%, rgb(250, 250, 250) 100%);
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
            content: '';
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
    .intro .slick-prev::before, .intro .slick-next::before {
        font-size: 40px;
    }
</style>