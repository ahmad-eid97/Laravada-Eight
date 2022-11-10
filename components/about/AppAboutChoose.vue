<template>
    <div class="choose-area">
        <div class="row m-0">
            <div class="col-lg-6 text">
                <div class="choose-content mr-20">
                    <div class="section-title">
                        <span class="sp-color1">Why Choose Us</span>
                        <h2>We Provide Truly Prominent It Solutions.</h2>
                        <p>
                        Aenean sollicitudin, lorem quis bibendum auctor, nisi elit consequat ipsum, nec sagittis sem nibh id elit. Duis sed odio sit amet nibh vulputate cursus a sit amet mauris. Morbi accumsan ipsum auctor a ornare odio.
                        </p>
                    </div>
                    <div class="row">
                        <div class="col-lg-6 col-6">
                            <div class="choose-content-card">
                                <div class="content">
                                    <font-awesome-icon icon="fa-solid fa-hand-holding-hand" />
                                    <h3>Experience</h3>
                                </div>
                                <p>Neque porro quisquam est qui dolorem ipsum quia dolor sit amet</p>
                            </div>
                        </div>
                        <div class="col-lg-6 col-6">
                            <div class="choose-content-card">
                                <div class="content">
                                    <font-awesome-icon icon="fa-solid fa-circle-question" />
                                    <h3>Quick Support</h3>
                                </div>
                                <p>Neque porro quisquam est qui dolorem ipsum quia dolor sit amet</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-6 image">
                <div class="overlay"></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppAboutChoose'
}
</script>

<style>
.choose-area {
    background-color: #f5f5f5;
}
.choose-area .text {
    padding: 120px 60px;
}
.choose-area .image {
    background-image: url(https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-25-1.jpg);
    position: relative;
    background-position-x: 50%;
    background-position-y: 50%;
    background-size: cover;
    box-sizing: border-box;
}
.choose-area .image .overlay {
  background-image: linear-gradient(270deg,transparent 50%,#f5f5f5);
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}
.choose-area .choose-content {
    margin-bottom: 30px;
    margin-right: 20px;
}
.choose-area .section-title {
  margin: 0 auto ;
  padding: 0;
  position: relative;
  text-align: start;
}
.choose-area .section-title span {
    margin-bottom: 8px;
    font-weight: 600;
    display: block;
    color:#222;
}
.choose-content .section-title h2 {
    color: #222;
    font-size: 36px;
    font-weight: 600;
    line-height: 43.2px;
    padding: 0 0 30px;
    text-align: left;
    margin-top: 10px;
    margin-right: 0px;
    margin-bottom: 15px;
    margin-left: 0px;
}
.choose-area .choose-content .section-title p {
    color: #222;
    padding-top: 10px;
    margin-bottom: 0;
    max-width: 530px;
}
.choose-area .choose-content .choose-content-card {
    margin-top: 15px;
}
.choose-area .choose-content .choose-content-card .content {
    padding-top: 20px;
    position: relative;
    padding-left: 75px;
}
.choose-area .choose-content .choose-content-card .content svg {
    position: absolute;
    top: 10px;
    left: 0;
    font-size: 60px;
    color:var(--main-color);
    line-height: 1;
}
.choose-area .choose-content .choose-content-card .content h3 {
    margin-top: 10px;
    margin-bottom: 30px;
    font-weight: 600;
    color: #222;
    font-size: 22px;
}
.choose-area .choose-content .choose-content-card p {
    margin-top: 5px;
    margin-bottom: 0;
    color: #222;
}
.choose-area .choose-img {
    margin-bottom: 30px;
}
.choose-area .choose-img img {
  border-radius: 15px;
}
</style>