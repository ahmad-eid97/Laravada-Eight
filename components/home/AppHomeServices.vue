<template>
  <section class="services pb-90">
    <div class="row">
      <h2>Services we offer</h2>
    </div>
    <div class="row m-0" v-if="services.length >= 1">
      <div
        v-for="service in services.slice(0, 4)"
        :key="service.id"
        class="col-md-12 col-lg-6 mb-5"
      >
        <div class="item">
          <div class="row m-0 justify-content-center align-items-center">
            <div class="col-auto">
              <div class="image">
                <img :src="service.image" :alt="service.title" />
              </div>
            </div>
            <div class="col">
              <h4>{{ services.title }}</h4>
              <p>
                {{ service.short_description }}
              </p>
              <nuxt-link :to="`/service/${service.id}`" class="btn"
                >Details</nuxt-link
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeServices",
  props: ["services"],
  data() {
    return {};
  },
  methods: {},
};
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
  position: relative;
  overflow: hidden;
  display: grid;
  place-items: center;
}
.services .item .image img {
  max-height: 100%;
  width: 100px;
  object-fit: contain;
}
.services .item .image:after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 1;
  background-image: linear-gradient(
    rgba(0, 0, 0, 0) 0%,
    rgba(0, 0, 0, 0.5) 100%
  );
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
