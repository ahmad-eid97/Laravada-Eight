<template>
  <header
    :class="!topOfPage ? 'onScroll' : ''"
    class="header header-style-2 clearfix"
  >
    <div class="cart" :class="openCart ? 'opened' : ''">
      <div class="head">
        <i class="fa-regular fa-xmark" @click="openCart = false"></i>
        <button
          @click="goToCheckout"
          :disabled="$store.state.cartItems.length <= 0"
        >
          <i class="fa-regular fa-badge-check"></i> Checkout
        </button>
      </div>
      <cart />
    </div>
    <div class="row m-0 w-100">
      <app-top-bar class="col-12 topBar"></app-top-bar>
      <b-navbar toggleable="lg">
        <b-navbar-brand :href="localePath('/')">
          <img
            src="/assets/images/logo.png"
            alt="logoImage"
            style="maxwidth: 200px !important"
          />
        </b-navbar-brand>

        <div class="d-flex align-items-center gap-3 smallScr">
          <lang-switch></lang-switch>
          <div class="m-0 cartIcon" @click="openCart = !openCart">
            <span>{{ $store.state.cartItems.length }}</span>
            <i class="fa-regular fa-cart-plus"></i>
          </div>
          <div v-if="$store.state.user" class="logout" @click="logout">
            <i class="fa-regular fa-right-from-bracket"></i>
          </div>
          <b-navbar-toggle target="navbar-toggle-collapse">
            <template #default="{ expanded }">
              <span
                class="menu-trigger"
                :class="expanded ? 'active' : ''"
                id="menu03"
              >
                <p></p>
                <p></p>
                <p></p>
              </span>
            </template>
          </b-navbar-toggle>
        </div>

        <b-collapse
          id="navbar-toggle-collapse"
          class="ml-auto justify-content-end"
          is-nav
        >
          <b-navbar-nav class="align-items-center">
            <b-nav-item active-class="active" :to="localePath('/')" exact
              >Home</b-nav-item
            >
            <b-nav-item active-class="active" :to="localePath('/about')"
              >About</b-nav-item
            >
            <b-nav-item active-class="active" :to="localePath('/team')"
              >Team</b-nav-item
            >
            <b-nav-item active-class="active" :to="localePath('/services')"
              >Services</b-nav-item
            >
            <b-nav-item active-class="active" :to="localePath('/testimonials')"
              >Projects</b-nav-item
            >
            <b-nav-item active-class="active" :to="localePath('/blogs')"
              >News</b-nav-item
            >
            <b-nav-item active-class="active" :to="localePath('/careers')"
              >Career</b-nav-item
            >
            <b-nav-item active-class="active" :to="localePath('/events')"
              >Events</b-nav-item
            >
            <b-nav-item active-class="active" :to="localePath('/contact')"
              >Contact</b-nav-item
            >
            <b-nav-item
              active-class="active"
              :to="localePath('/login')"
              v-if="$store.state.user"
              @click="logout"
              class="outLarge"
              >Logout</b-nav-item
            >

            <div class="d-flex align-items-center gap-3 largeScr">
              <div class="m-0 cartIcon" @click="openCart = !openCart">
                <span>{{ $store.state.cartItems.length }}</span>
                <i class="fa-regular fa-cart-plus"></i>
              </div>
              <div v-if="$store.state.user" class="logout" @click="logout">
                <i class="fa-regular fa-right-from-bracket"></i>
              </div>
            </div>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </header>
</template>

<script>
import LangSwitch from "../langSwitch/langSwitch.vue";
import cart from "../cart/cart.vue";
import AppTopBar from "./AppTopBar.vue";
export default {
  name: "AppHeader",
  components: {
    AppTopBar,
    cart,
    LangSwitch,
  },
  data() {
    return {
      topOfPage: true,
      openCart: false,
    };
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  mounted() {},
  methods: {
    logout() {
      this.$store.commit("setUserData", null);
      this.$cookies.remove("cms-auth");
      this.$cookies.remove("cms-user");
      this.$router.push(this.localePath("/login"));
    },
    handleScroll() {
      if (window.pageYOffset > 30) {
        if (this.topOfPage) this.topOfPage = false;
      } else {
        if (!this.topOfPage) this.topOfPage = true;
      }
    },
    goToCheckout() {
      this.openCart = false;
      this.$router.push("/checkout");
    },
  },
};
</script>
<style lang="scss">
header {
  position: fixed;
  left: 0;
  right: 0;
  z-index: 10;
  background-image: linear-gradient(180deg, #00000080 0%, #00000000 100%);
  .cart {
    width: 390px;
    height: 100vh;
    position: fixed;
    top: 0;
    right: 0;
    transform: translateX(390px);
    background-color: #fff;
    z-index: 999999;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.2);
    .head {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 10px;
      & > i {
        border: 1px solid var(--main-color);
        border-radius: 5px;
        width: 30px;
        height: 30px;
        display: grid;
        place-items: center;
        cursor: pointer;
        background-color: var(--main-color);
        color: #fff;
        &:hover {
          color: var(--main-color);
          background: transparent;
        }
      }
      button {
        padding: 5px 30px;
        font-size: 1.1rem;
        background-color: var(--main-color);
        color: #fff;
        border: 1px solid var(--main-color);
        display: flex;
        align-items: center;
        gap: 5px;
        i {
          font-size: 1.1rem;
        }
        &:disabled {
          opacity: 0.5;
          cursor: not-allowed;
          &:hover {
            background-color: var(--main-color);
            color: #fff;
          }
        }
        &:hover {
          background-color: transparent;
          color: var(--main-color);
        }
      }
    }
    &.opened {
      transform: translateX(0);
    }
    @include xs {
      width: 350px;
    }
  }
  .cartIcon {
    border: 1px solid #fff;
    border-radius: 5px;
    width: 45px;
    height: 45px;
    display: grid;
    place-items: center;
    cursor: pointer;
    position: relative;
    span {
      position: absolute;
      top: -15px;
      right: -10px;
      width: 30px;
      height: 30px;
      background-color: var(--main-color);
      border-radius: 50%;
      color: #fff;
      display: grid;
      place-content: center;
      font-size: 1.2rem;
      @include sm {
        font-size: 1rem;
      }
    }
    i {
      color: #fff;
    }
    @include sm {
      width: 40px;
      height: 40px;
      margin: 0 10px !important;
    }
    &:hover {
      background-color: var(--main-color);
      border-color: var(--main-color);
      i {
        color: #fff;
      }
    }
  }
}
.outLarge {
  display: none;
  @include md {
    display: inline;
  }
}
.logout {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: var(--main-color);
  color: #fff;
  display: grid;
  place-items: center;
  font-size: 1.2rem;
  margin: 0 15px !important;
  cursor: pointer;
  @include md {
    display: none;
  }
}
.smallScr {
  align-items: center;
  display: none !important;
  @include md {
    display: flex !important;
  }
}
.largeScr {
  align-items: center;
  display: flex !important;
  @include md {
    display: none !important;
  }
}
.onScroll {
  position: fixed;
  width: 100%;
  // height: 70px;
  min-height: 80px;
  display: flex;
  align-items: center;
  transition: all 0.2s ease-in-out;
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
.navbar-toggler {
  margin: 0;
}
.onScroll .cartIcon {
  border: 1px solid var(--main-color);
  i {
    color: var(--main-color);
  }
  &:hover {
    background-color: var(--main-color);
    border-color: var(--main-color);
    i {
      color: #fff;
    }
  }
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
.navbar {
  @include sm {
    padding: 20px !important;
  }
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
  line-height: 22.1px;
}
.navbar .nav-item .nav-link.active {
  color: rgb(48, 164, 108);
  display: block;
  font-size: 17px;
  font-weight: 600;
  line-height: 22.1px;
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
