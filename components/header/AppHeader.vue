<template>
    <header :class="!topOfPage ? 'onScroll' : ''" class="header header-style-2 clearfix">
        <div class="row m-0 w-100">
            <app-top-bar class="col-12 topBar"></app-top-bar>
            <b-navbar toggleable="lg">
                <b-navbar-brand href="#">
                    <img src="/assets/images/logo.png" alt="logoImage" style="maxWidth: 200px !important">
                </b-navbar-brand>

                <b-navbar-toggle target="navbar-toggle-collapse">
                    <template #default="{ expanded }">
                        <span class="menu-trigger" :class="expanded ? 'active' : ''" id="menu03">
                            <p></p>
                            <p></p>
                            <p></p>
                        </span>
                    </template>
                </b-navbar-toggle>

                <b-collapse id="navbar-toggle-collapse" class="ml-auto justify-content-end" is-nav>
                    <b-navbar-nav class="align-items-center">
                        <b-nav-item active-class="active" :to="localePath('/')" exact>Home</b-nav-item>
                        <b-nav-item active-class="active" :to="localePath('/about')">About</b-nav-item>
                        <b-nav-item active-class="active" :to="localePath('/team')">Team</b-nav-item>
                        <b-nav-item active-class="active" :to="localePath('/services')">Services</b-nav-item>
                        <b-nav-item active-class="active" :to="localePath('/testimonials')">Projects</b-nav-item>
                        <b-nav-item active-class="active" :to="localePath('/blogs')">News & articles</b-nav-item>
                        <b-nav-item active-class="active" :to="localePath('/contact')">Contact</b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
            </b-navbar>
        </div>
    </header>
</template>

<script>
import AppTopBar from './AppTopBar.vue'
export default {
    name: 'AppHeader',
    components: {
        AppTopBar,
    },
    data() {
        return {
            topOfPage: true
        }
    },
    beforeMount() {
        window.addEventListener('scroll', this.handleScroll)
    },
    mounted() {
    },
    methods: {
        handleScroll(){
            if(window.pageYOffset>30){
                if(this.topOfPage) this.topOfPage = false
            } else {
                if(!this.topOfPage) this.topOfPage = true
        }
        }
    }
}
</script>
<style lang="scss">
    header {
        position: fixed;
        left: 0;
        right: 0;
        z-index: 10;
        background-image: linear-gradient(180deg,#00000080 0%,#00000000 100%);
    }
    .onScroll {
        position: fixed;
        width: 100%;
        // height: 70px;
        min-height: 80px;
        display: flex;
        align-items: center;
        transition: all .2s ease-in-out;
        box-shadow: 0 0 10px #aaa;
        background-color: #fff;
        top: 0;
        z-index: 10;
        background-image: none;
    }
    .onScroll .top-bar {
        overflow: hidden;
        height: 0px;
        padding: 0px;
    }
    .onScroll .social-icon {
        display: none;
    }
    nav {
        padding: 20px 60px 0 !important;
    }
    .onScroll nav {
        padding: 0 60px 0 !important;
    }
    .navbar-brand {
        width: 100px;
        transition: all 0.3s linear;

    }
    .onScroll .navbar-brand {
        width: 70px;

    }
    .navbar .nav-item {
        padding: 0 16px;
    }
    .navbar .nav-item .nav-link {
        color: #fff;
        display: block;
        font-size: 17px;
        font-weight: 600;
        line-height: 22.1px;
        padding: 0;
    }
    .onScroll .navbar .nav-item .nav-link {
        color: #000;
    }
    .navbar .nav-item .nav-link:hover,
    .navbar .nav-item .nav-link.link {
        color: rgb(48, 164, 108);
        display: block;
        font-size: 17px;
        font-weight: 600;
        line-height: 22.1px
    }
    .navbar .nav-item .nav-link.active {
        color: rgb(48, 164, 108);
        display: block;
        font-size: 17px;
        font-weight: 600;
        line-height: 22.1px
    }
    .navbar-toggler {
        border: 3px solid var(--main-color);
        outline: none;
    }
    .menu-trigger p {
        width: 30px;
        height: 5px;
        background: var(--main-color);
        margin: 0 0 2px;
    }
    button {
        outline: none !important;
        box-shadow: unset !important;
    }
    @include md {
        .topBar {
            display: none;
        }
        .onScroll .navbar-nav {
            transform: translateY(50px);
        }
        .navbar-nav {
            background: #fff;
            padding: 20px 0;
            transform: translateY(20px);
        }
        .navbar-nav li {
            padding: 5px 0 !important;
        }
        .navbar-nav li.nav-item a {
            color: var(--main-color) !important;
        }
    }
</style>