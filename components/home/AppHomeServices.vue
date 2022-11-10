<template>
    <section class="services pb-90">
        <div class="row">
            <h2>Services we offer</h2>
        </div>
        <div class="row m-0">
            <div class="col-md-12 col-lg-6 mb-5">
                <div class="item">
                    <div class="row m-0 justify-content-center">
                        <div class="col-auto">
                            <div class="image">
                                <img src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-1-1.jpg" alt="">
                            </div>
                        </div>
                        <div class="col">
                            <h4>Accounting services</h4>
                            <p>
                                Ut sit amet semper arcu. Proin eget ex viverra lorem pretium. Morbi dapibus a tellus at euismod. Ut sit amet semper!
                            </p>
                            <a href="#" class="btn">Details</a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-12 col-lg-6 mb-5">
                <div class="item">
                    <div class="row m-0 justify-content-center">
                        <div class="col-auto">
                            <div class="image">
                                <img src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-6-1.jpg" alt="">
                            </div>
                        </div>
                        <div class="col">
                            <h4>Project management</h4>
                            <p>
                                Ut sit amet semper arcu – dolor proin eget ex convallis eu viverra lorem pretium. Morbi dapibus a euismod lorem ipsum dolor.
                            </p>
                            <a href="#" class="btn">Details</a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-12 col-lg-6 mb-5">
                <div class="item">
                    <div class="row m-0 justify-content-center">
                        <div class="col-auto">
                            <div class="image">
                                <img src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/01/img001-8-1.jpg" alt="">
                            </div>
                        </div>
                        <div class="col">
                            <h4>Networks & communications</h4>
                            <p>
                                Ut sit amet semper arcu. Proin eget ex convallis eu viverra lorem pretium. Morbi dapibus a tellus.
                            </p>
                            <a href="#" class="btn">Details</a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-12 col-lg-6 mb-5">
                <div class="item">
                    <div class="row m-0 justify-content-center">
                        <div class="col-auto">
                            <div class="image">
                                <img src="https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-25-1.jpg" alt="">
                            </div>
                        </div>
                        <div class="col">
                            <h4>B2B Solutions</h4>
                            <p>
                                Ut sit amet arcu – dolor proin eget ex convallis eu viverra lorem pretium. Morbi dapibus at euismod lorem ipsum dolor.
                            </p>
                            <a href="#" class="btn">Details</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>

export default {
    name: 'AppHomeServices',
    data() {
        return {
            
        }
    },
    methods : {
        
    }
}
</script>
<style lang="scss">
    .services {
        padding: 30px 60px 90px;
    }
    .services h2 {
        color: rgb(34, 34, 34);
        font-size: 36px;
        font-weight: 600;
        line-height: 43.2px;
        padding: 0 30px 30px;
        text-align: center;
    }
    .services .item .image {
        width: 220px;
        height: 220px;
        border-radius: 50%;
    }
    .services .item .image {
        width: 220px;
        height: 220px;
        border-radius: 50%;
        position: relative;
        overflow: hidden;
    }
    .services .item .image img {
        max-height: 100%;
    }
    .services .item .image:after {
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
    @include xs {
        .services .item {
            text-align: center;
        }
    }
    .services .item .image:hover::after {
        opacity: 0.9;
    }

    .services .item h4 {
        color: rgb(34, 34, 34);
        font-size: 22px;
    }
    .services .item p {
        color: rgb(102, 102, 102);
        font-size: 17px;
        font-weight: 400;
        line-height: 27.2px;
        margin-top: 15px;
        margin-bottom: 0;
    }
    
    .services .item .btn {
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
        margin-top: 20px;
        min-width: 80px;
    }
    .services .item .btn:hover {
       background-color: rgb(40, 134, 89);
    }
</style>