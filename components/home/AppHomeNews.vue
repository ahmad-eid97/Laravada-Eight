<template>
    <section class="blog-section ">
        <div class="container">
            <div class="row">
                <div class="section-title">

                    <h2>RECENT NEWS & EVENTS</h2>

                </div>
            </div>
            <div class="row">
                <div class="col-md-6 col-lg-4 news-carousel">
                    <carousel :items='1' :dots='false'>
                        <div class="item">
                            <div class=" events-col">

                                <div class="thumb">
                                    <img src="" alt="">
                                </div>
                                <div class="content">
                                    <h3>OCT. 18-21 2017 / PARIS</h3>
                                    <h4>EUROPEAN BUSINESS FORUM</h4>

                                    <h6>Donec vestibulum lectus sem, vel convallis ligula commodo ac. Aenean congue
                                        placerat risus, eu ullamcorper velit maximus sed.</h6>
                                        <a href="#" class="btn">VIEW DETAILS</a>


                                </div>
                            </div>
                        </div>
                        <div class="item">
                            <div class=" events-col">

                                <div class="thumb">
                                    <img src="" alt="">
                                </div>
                                <div class="content">
                                    <h3>OCT. 18-21 2017 / PARIS</h3>
                                    <h4>EUROPEAN BUSINESS FORUM</h4>

                                    <h6>Donec vestibulum lectus sem, vel convallis ligula commodo ac. Aenean congue
                                        placerat risus, eu ullamcorper velit maximus sed.</h6>
                                        <a href="#" class="btn">VIEW DETAILS</a>


                                </div>
                            </div>
                        </div>
                    </carousel>
                    <font-awesome-icon class="next" icon="fa-solid fa-angle-right" />
                    <font-awesome-icon class="prev" icon="fa-solid fa-angle-left" />
                </div>
                <div class="col-md-6 col-lg-8">

                    <div class="row">
                        <div class=" col-lg-4">
                            <div class="events">
                                <div class="thumb">
                                    <img alt="" src="">
                                </div>

                                <div class="content mt-40 right">
                                    <h3>Quisque at nibh ac purus aliquet accumsan</h3>

                                    <p>Amet ipsum id sem quis mauris porttitor conse quat id vitae dolor. Phasellus
                                        ligula velit molestie rhoncus ullamcorper mauris ultricies mi at pharetra
                                        lorem.</p>
                                </div>
                                <a href="" class="read-btn float-end">Read more
                                    <font-awesome-icon icon="fa-solid fa-caret-right" />
                                </a>
                            </div>

                        </div>
                        <div class=" col-lg-4">
                            <div class="events">
                                <div class="thumb">
                                    <img alt="" src="">
                                </div>

                                <div class="content mt-40 right">
                                    <h3>Sed tincidunt urna sit amet tempus euismod</h3>

                                    <p>Amet ipsum id sem quis mauris porttitor conse quat id vitae dolor. Phasellus
                                        ligula velit molestie rhoncus ullamcorper mauris ultricies mi at pharetra
                                        lorem.</p>
                                </div>
                                <a href="" class="read-btn float-end">Read more
                                    <font-awesome-icon icon="fa-solid fa-caret-right" />
                                </a>
                            </div>

                        </div>
                        <div class=" col-lg-4">
                            <div class="events">
                                <div class="thumb">
                                    <img alt="" src="">
                                </div>

                                <div class="content mt-40 right">
                                    <h3>Proin ligula iaculis quis ornare id purus</h3>

                                    <p>Amet ipsum id sem quis mauris porttitor conse quat id vitae dolor. Phasellus
                                        ligula velit molestie rhoncus ullamcorper mauris ultricies mi at pharetra
                                        lorem.</p>
                                </div>
                                <a href="" class="read-btn float-end">Read more
                                    <font-awesome-icon icon="fa-solid fa-caret-right" />
                                </a>
                            </div>

                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import carousel from 'vue-owl-carousel'

export default {
    name: 'AppHomeNews',
    components: {carousel},
    data() {
        return {
            
        }
    },
    methods : {
        
    }
}
</script>

<style>
    .events .svg-inline--fa {
    
    vertical-align: -2px;
    }
    .news-carousel {
        position: relative;
    }
    .news-carousel .owl-carousel {
        background-color: #f5f5f5;
    }
    .news-carousel .owl-carousel .owl-item {
        padding: 35px 35px;
    }
    .news-carousel .btn ,
    .news-carousel .btn:hover {
        background-color: #ffb536;
        border-radius: 0;
        color: #fff;
        padding: 10px 16px;
        font-weight: bold;
        border: none;
    }
    .news-carousel .owl-theme .owl-nav .owl-next,
    .news-carousel .owl-theme .owl-nav .owl-next:hover, 
    .news-carousel .owl-theme .owl-nav .owl-prev, 
    .news-carousel .owl-theme .owl-nav .owl-prev:hover {
        background-color: #ffb536;
        color: transparent;
        display: inline-block;
        height: 75px;
        width: 24px;
        top: 197px;
        text-align: center;
        line-height: 75px;
        font-size: 18px;
        position: absolute;
    }
    .news-carousel .owl-nav .owl-next {
        right: 0px;
    }
    .news-carousel .owl-nav .owl-prev {
        left: 0px;
    }
    .next {
        display: inline-block;
        top: 232px;
        text-align: center;
        line-height: 75px;
        font-size: 18px;
        position: absolute;
        color: #fff;
        right: 24px;
        z-index: 2;
    }
    .prev {
        display: inline-block;
        top: 232px;
        text-align: center;
        line-height: 75px;
        font-size: 18px;
        position: absolute;
        color: #fff;
        left: 24px;
        z-index: 2;
    }
    
</style>