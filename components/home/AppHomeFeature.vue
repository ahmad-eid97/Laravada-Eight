<template>
    <section class="features">
        <div class="container">
            <div class="row gy-4 justify-content-center">

                <div class="col">
                    <div class="item ">
                        <font-awesome-icon icon="fa-solid fa-rocket" />
                        <div class="content">
                            <h6 class="reward-h6">
                                 Innovative approach 
                            </h6>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="item ">
                        <font-awesome-icon icon="fa-solid fa-user-tie" />
                        <div class="content">
                            <h6 class="reward-h6">
                                 Top industry specialists
                            </h6>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="item ">
                        <font-awesome-icon icon="fa-solid fa-list-check" />
                        <div class="content">
                            <h6 class="reward-h6">
                                 Perfect timing
                            </h6>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="item ">
                        <font-awesome-icon icon="fa-solid fa-headset" />
                        <div class="content">
                            <h6 class="reward-h6">
                                 24/7 Customer support 
                            </h6>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="item ">
                        <font-awesome-icon icon="fa-solid fa-dollar-sign" />
                        <div class="content">
                            <h6 class="reward-h6">
                                 Reasonable prices
                            </h6>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="item ">
                        <font-awesome-icon icon="fa-solid fa-award" />
                        <div class="content">
                            <h6 class="reward-h6">
                                 Money back guarantee 
                            </h6>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>


export default {
    name: 'AppHomeFeature',
    components: {},
    data() {
        return {
            
        }
    },
    methods : {
        
    }
}
</script>
<style>
    .features {
        padding: 60px;
    }
    .features .item {
        text-align: center;
    }
    .features .item svg {
        color: rgb(48, 164, 108);
        display: flex;
        font-size: 32px;
        hyphens: manual;
        letter-spacing: normal;
        margin: 0 auto 15px
    }
    .features .item h6 {
        color: rgb(34, 34, 34);
        font-size: 19px;
        font-weight: 600;
        line-height: 26.6px;
    }
</style>