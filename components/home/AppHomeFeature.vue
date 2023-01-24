<template>
  <section class="features">
    <div class="container">
      <div
        class="row gy-4 justify-content-center"
        v-if="features.find((one) => one.key === 'features_text_list').value"
      >
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
  mounted() {
    document
      .querySelector(".features")
      .style.setProperty(
        "--features-bg",
        this.features.find(
          (one) => one.key === "features_background_active_section"
        ).value === "color"
          ? this.features.find(
              (one) => one.key === "features_background_color_section"
            ).value
          : `url(${
              this.features.find(
                (one) => one.key === "features_background_image_section"
              ).value
            })`
      );

    document
      .querySelector(".features")
      .style.setProperty(
        "--features-fontSize",
        `${
          this.features.find((one) => one.key === "features_font_size_section")
            .value
        }px`
      );

    if (
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ) &&
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ).value === "both"
    ) {
      document
        .querySelector(".features")
        .style.setProperty(
          "--features-border-top",
          `${
            this.features.find(
              (one) => one.key === "features_border_size_section"
            ).value
          }px ${
            this.features.find(
              (one) => one.key === "features_border_type_section"
            ).value
          } ${
            this.features.find(
              (one) => one.key === "features_border_color_section"
            ).value
          }`
        );

      document
        .querySelector(".features")
        .style.setProperty(
          "--features-border-bottom",
          `${
            this.features.find(
              (one) => one.key === "features_border_size_section"
            ).value
          }px ${
            this.features.find(
              (one) => one.key === "features_border_type_section"
            ).value
          } ${
            this.features.find(
              (one) => one.key === "features_border_color_section"
            ).value
          }`
        );
    } else if (
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ) &&
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ).value === "top"
    ) {
      document
        .querySelector(".features")
        .style.setProperty(
          "--features-border-top",
          `${
            this.features.find(
              (one) => one.key === "features_border_size_section"
            ).value
          }px ${
            this.features.find(
              (one) => one.key === "features_border_type_section"
            ).value
          } ${
            this.features.find(
              (one) => one.key === "features_border_color_section"
            ).value
          }`
        );
    } else if (
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ) &&
      this.features.find(
        (one) => one.key === "features_border_position_section"
      ).value === "bottom"
    ) {
      document
        .querySelector(".features")
        .style.setProperty(
          "--features-border-bottom",
          `${
            this.features.find(
              (one) => one.key === "features_border_size_section"
            ).value
          }px ${
            this.features.find(
              (one) => one.key === "features_border_type_section"
            ).value
          } ${
            this.features.find(
              (one) => one.key === "features_border_color_section"
            ).value
          }`
        );
    }
  },
};
</script>
<style lang="scss">
.features {
  padding: 60px;

  --features-bg: #fff;
  --features-fontSize: 20px;
  --features-border-top: 0px solid #fff;
  --features-border-bottom: 0px solid #fff;

  background: var(--features-bg);
  border-top: var(--features-border-top);
  border-bottom: var(--features-border-bottom);
  background-repeat: no-repeat;
  background-size: cover;
  h2 {
    font-size: var(--features-fontSize);
  }
}
.features .item {
  text-align: center;
  display: flex;
  justify-content: center;
  flex-direction: column;
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
