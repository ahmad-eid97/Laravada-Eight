<template>
   <section class="contact-divider">
       <div class="row m-0">
           <div class="col-lg-6 text">
               <h3>
                   Not sure what fits your business needs? Get free consultation!
               </h3>
               <p>
                   Experience you can trust, service you can count on. Seven Company – your partners in profit!
               </p>
               <div class="form">
                   <div class="row m-0">
                       <div class="col" style="padding-left: 0">
                           <div class="form-group">
                               <label for="">Name <span style="color:var(--main-color)">*</span></label>
                               <input type="text" class="form-control">
                           </div>
                       </div>
                       <div class="col" style="padding-right: 0">
                           <div class="form-group">
                               <label for="">Phone</label>
                               <input type="text" class="form-control">
                           </div>
                       </div>
                       <div class="col-12 p-0">
                           <a href="#" class="btn">
                               <font-awesome-icon icon="fa-solid fa-phone" />
                               Request a call-back
                           </a>
                       </div>
                   </div>
               </div>
           </div>
           <div class="col-lg-6 image">
            <div class="overlay">

            </div>
           </div>
       </div>
    </section>
</template>

<script>

export default {
    name: 'AppHomeContactDivider',
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
    .contact-divider {
        background-color: rgb(245, 245, 245)
    }
    .contact-divider .image {
        background-image: url("https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-25-1.jpg");
        position: relative;
        background-position-x: 50%;
        background-position-y: 50%;
        background-size: cover;
        box-sizing: border-box;
        min-height: 400px;
    }
    .contact-divider .image .overlay {
        background-image: linear-gradient(270deg, rgba(0, 0, 0, 0) 50%, rgb(245, 245, 245) 100%);
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;

    }
    .contact-divider .text {
        padding: 120px 60px;
    }
    @include md {
        .contact-divider .text {
            padding: 50px 40px;
        }
    }
    .contact-divider .text h3 {
        color: rgb(34, 34, 34);
        font-size: 28px;
        font-weight: 600;
        line-height: 36.4px;
        margin-bottom: 30px;
    }
    .contact-divider .text p {
        color: rgb(102, 102, 102);
        font-size: 19px;
        margin-bottom: 30px;
    }
    .contact-divider label {
        box-sizing: border-box;
        color: rgb(34, 34, 34);
        font-size: 17px;
        padding-bottom: 5px;
    }
    .contact-divider input {
        background-color: rgb(255, 255, 255);
        border-radius: 2px;
        border: 1px solid rgba(0, 0, 0, 0.12);
        color: rgb(102, 102, 102);
        font-size: 16px;
        height: 47px;
        line-height: 22.4px;
        max-width: 100%;
        min-height: 47px;
        outline-color: rgb(102, 102, 102);
        padding-bottom: 6px;
        padding-left: 16px;
        padding-right: 16px;
        padding-top: 6px;
        transition-delay: 0s;
        transition-duration: 0.3s;
        transition-property: all;
        vertical-align: middle;
        box-shadow: none;
        margin-bottom: 30px;
    }
    .contact-divider input:focus {
       box-shadow: none;
       border-color: var(--main-color);
    }
    .contact-divider .btn {
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
    .contact-divider .btn svg {
        margin-right: 12px;
    }
    .contact-divider .btn:hover {
        border: none;
       background-color: rgb(40, 134, 89);
       color: #fff;
    }
</style>