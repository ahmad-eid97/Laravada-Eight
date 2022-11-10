<template>
  <section class="testimonials">
        <div class="row mb-3">
            <h2>Why choose our company</h2>
        </div>
        <div class="row">
            <div class="col-lg-8">
                <div class="row m-0 h-100">
                    <div class="col-md-6 item">
                        <font-awesome-icon icon="fa-solid fa-user-tie" />
                        <h4>Brilliant team</h4>
                        <p>
                            Maecenas gravida lacus luctus nec tique eget sed, viverra at sapiengravid nec dolor suscipit ristique eget - malesuada sed viverra.
                        </p>
                    </div>
                    <div class="col-md-6 item">
                        <font-awesome-icon icon="fa-solid fa-arrows-rotate" />
                        <h4>Rich experience</h4>
                        <p>
                            Dolor sit amet - onsectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus glavrida.
                        </p>
                    </div>
                    <div class="col-md-6 item">
                        <font-awesome-icon icon="fa-solid fa-life-ring" />
                        <h4>24/7 online support</h4>
                        <p>
                            Nullam arcu onsectetur adipiscing elit. Ut elit tellus, luctus nec tique eget sed, viverra at sapiengravida lacus nec dolor suscipit faucibus.
                        </p>
                    </div>
                    <div class="col-md-6 item">
                        <font-awesome-icon icon="fa-solid fa-dollar-sign" />
                        <h4>Affordable prices</h4>
                        <p>
                            Etiam sit amet viverra at sapiengravid nec dolor suscipit convallis erat. Class aptent taciti sociosqu ad litora torquent per conubia!
                        </p>
                    </div>
                </div>

            </div>
            <div class="col-lg-4">
                <div class="founder">
                    <div class="image">
                        <img src="https://the7.io/elementor-business/wp-content/uploads/sites/89/elementor/thumbs/3-2-1-oog1pthotm2l1rtpd9yemm3n1pzowgm9h0mcd4ekqw.jpg" alt="">
                    </div>
                    <p>
                        “Thoughts are things! And powerful things at that, when mixed with definiteness of purpose, and burning desire, can be translated into riches.”
                    </p>
                    <h4>Alexandra Blackfire</h4>
                    <h5>Co-founder, CEO</h5>
                </div>
            </div>
        </div>
  </section>
</template>

<script>

export default {
    name: 'AppHometestimonials',
    components: {},
    data() {
        return {
            show: 'show1'
        }
    },
    mounted() {
        this.autoPlay();
    },
    methods: {
        autoPlay() {
            var items = ['show1', 'show2', 'show3', 'show4', 'show5'];
            var item = ''
            let _this = this
            setInterval(function() { 
                
                item = items[Math.floor(Math.random()*items.length)];
                _this.showData(item);
            }, 5000);
        },
        showData(show) {
            this.show = show
        }
    }
}
</script>

<style>
    .testimonials {
        padding: 90px 30px;
    }
    .testimonials h2 {
        color: rgb(34, 34, 34);
        font-size: 36px;
        font-weight: 600;
        line-height: 43.2px;
        padding: 0 30px 30px;
        text-align: center;
    }
    .testimonials .item .number {
        color: rgb(48, 164, 108);
        font-size: 100px;
        font-weight: 100;
        line-height: 80px;
        word-spacing: 0px;
    }
    .testimonials .item h3 {
        margin-top: 30px;
        color: rgb(34, 34, 34);
        font-size: 22px;
        font-weight: 600;
        line-height: 28.6px;
    }
    .testimonials .item p {
        margin-top: 15px;
        color: rgb(34, 34, 34);
        color: rgb(102, 102, 102);
        font-size: 17px;
    }
    .testimonials .founder {
        color: rgb(102, 102, 102);
        font-size: 17px;
        padding-bottom: 40px;
        padding-left: 30px;
        padding-right: 30px;
        padding-top: 40px;
        /* width: 342.6px; */
        background-color: rgb(245, 245, 245);
    }
    .testimonials .founder .image {
        text-align: center;
        margin-bottom: 30px;
    }
    .testimonials .founder .image img {
        width: 141px;
        height: 141px;
        border-radius: 50%;
        margin: 0 auto;
    }
    .testimonials .founder p {
        color: rgb(102, 102, 102);
        font-size: 19px;
        line-height: 30.4px;
        text-align: center;
        margin-bottom: 20px;
    }
    .testimonials .founder h4 {
        color: rgb(34, 34, 34);
        font-size: 19px;
        font-weight: 600;
        line-height: 26.6px;
        text-align: center;
        margin-bottom: 10px;
    }
    .testimonials .founder h5 {
        color: rgb(48, 164, 108);
        font-size: 17px;
        font-weight: 400;
        line-height: 27.2px;
        text-align: center;
    }
    .testimonials .item svg{
        color: rgb(48, 164, 108);
        display: block;
        font-size: 32px;
        font-weight: 900;
        height: 32px;
        line-height: 32px;
        margin-bottom: 20px;
        position: relative;
        text-align: center;
        width: 32px;
    }
    .testimonials .item h4{
        color: rgb(34, 34, 34);
        font-size: 22px;
        font-weight: 600;
        line-height: 28.6px;
        text-align: left;
    }
    .testimonials .item p{
        color: rgb(102, 102, 102);
        font-size: 17px;
        font-weight: 400;
        line-height: 27.2px;
        margin-top: 15px;
        text-align: left;
    }
</style>