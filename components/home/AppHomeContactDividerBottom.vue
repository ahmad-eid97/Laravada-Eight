<template>
   <section class="contact-divider-2">
       <div class="row m-0">
           <div class="col-md-6 text">
               <h3>
                   Bring your business to a new quality level! Get in touch now!
               </h3>
               <p>
                   <font-awesome-icon icon="fa-solid fa-phone" />
                   1 (234) 567-891
               </p>
               <a href="#" class="btn">
                    <font-awesome-icon icon="fa-solid fa-comment-dollar" />
                    Request for quote online
                </a>
           </div>
           <div class="col-md-6 image">
            <div class="overlay">

            </div>
           </div>
       </div>
    </section>
</template>

<script>

export default {
    name: 'AppHomeContactDividerBottom',
    components: {},
    data() {
        return {
            
        }
    },
    methods : {
        
    }
}
</script>

<style lang="scss">
    .contact-divider-2 {
        background-color: rgb(245, 245, 245)
    }
    .contact-divider-2 .image {
        background-image: url("https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-4-1.jpg");
        position: relative;
        background-position-x: 50%;
        background-position-y: 50%;
        background-size: cover;
        box-sizing: border-box;
        min-height: 400px;
    }
    .contact-divider-2 .image .overlay {
        background-image: linear-gradient(270deg, rgba(0, 0, 0, 0) 50%, rgb(245, 245, 245) 100%);
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;

    }
    .contact-divider-2 .text {
        padding: 120px 60px;
    }
    @include md {
        .contact-divider-2 .text {
            padding: 50px 40px;
        }
    }
    .contact-divider-2 .text h3 {
        color: rgb(34, 34, 34);
        font-size: 28px;
        font-weight: 600;
        line-height: 36.4px;
        margin-bottom: 30px;
        text-align: center;
    }
    .contact-divider-2 .text p {
        color: rgb(48, 164, 108);
        font-size: 28px;
        font-weight: 600;
        line-height: 36.4px;
        text-align: left;
        text-decoration-color: rgb(48, 164, 108);
        text-align: center;
    }
    
    .contact-divider-2 .btn {
        display: flex;
        margin-bottom: 30px;
        align-items: center;
        background-color: rgb(48, 164, 108);
        border-radius: 3px;
        box-shadow: rgba(0, 0, 0, 0) 0px 0px 10px 0px;
        color: rgb(255, 255, 255);
        flex-basis: 100%;
        font-size: 17px;
        font-weight: 600;
        letter-spacing: normal;
        line-height: 17px;
        min-height: 56px;
        min-width: 140px;
        padding-bottom: 10px;
        padding-left: 24px;
        padding-right: 24px;
        padding-top: 10px;
        text-decoration-color: rgb(255, 255, 255);
        transition: all 0.3s linear;
        justify-content: center;
        border: none;
    }
    .contact-divider-2 .btn svg {
        margin-right: 12px;
    }
    .contact-divider-2 .btn:hover {
        border: none;
       background-color: rgb(40, 134, 89);
       color: #fff;
    }
</style>