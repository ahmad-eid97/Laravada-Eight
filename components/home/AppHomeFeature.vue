<template>
  <section class="features">
    <div class="container">
      <div class="row gy-4 justify-content-center">
        <div
          v-for="feature in features
            .find((one) => one.key === 'features_text_list')
            .value.slice(0, 5)"
          :key="feature"
          class="col"
        >
          <div class="item">
            <i :class="feature.icon"></i>
            <div class="content">
              <h6 class="reward-h6">
                {{ feature.title }}
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
  name: "AppHomeFeature",
  props: ["features"],
  components: {},
  data() {
    return {};
  },
  methods: {},
};
</script>
<style>
.features {
  padding: 60px;
}
.features .item {
  text-align: center;
}
.features .item i {
  color: rgb(48, 164, 108);
  display: flex;
  font-size: 32px;
  hyphens: manual;
  letter-spacing: normal;
  margin: 0 auto 15px;
}
.features .item h6 {
  color: rgb(34, 34, 34);
  font-size: 19px;
  font-weight: 600;
  line-height: 26.6px;
}
</style>
