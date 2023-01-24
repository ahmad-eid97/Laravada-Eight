<template>
  <section class="contact-divider-2">
    <div class="row m-0">
      <div class="col-md-6 text">
        <h3>
          {{
            bottomBanner.find((one) => one.key === "banner-bottom_title").value
          }}
        </h3>
        <p>
          <i class="fa-solid fa-phone"></i>
          {{
            $store.state.websiteSettings.find(
              (one) => one.key === "contact_phone"
            ).plain_value
          }}
        </p>
        <a
          :href="
            bottomBanner.find((one) => one.key === 'banner-bottom_link').value
          "
          class="btn"
        >
          <i class="fa-solid fa-comment-dollar"></i>
          Request for quote online
        </a>
      </div>
      <div class="col-md-6 image">
        <div class="overlay"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeContactDividerBottom",
  props: ["bottomBanner"],
  components: {},
  data() {
    return {};
  },
  methods: {},
  mounted() {
    document
      .querySelector(".contact-divider-2")
      .style.setProperty(
        "--bannerBottom-bg",
        this.bottomBanner.find(
          (one) => one.key === "banner-bottom_background_active_section"
        ).value === "color"
          ? this.bottomBanner.find(
              (one) => one.key === "banner-bottom_background_color_section"
            ).value
          : `url(${
              this.bottomBanner.find(
                (one) => one.key === "banner-bottom_background_image_section"
              ).value
            })`
      );

    document
      .querySelector(".contact-divider-2")
      .style.setProperty(
        "--bannerBottom-fontSize",
        `${
          this.bottomBanner.find(
            (one) => one.key === "banner-bottom_font_size_section"
          ).value
        }px`
      );

    if (
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ) &&
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ).value === "both"
    ) {
      document
        .querySelector(".contact-divider-2")
        .style.setProperty(
          "--bannerBottom-border-top",
          `${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_size_section"
            ).value
          }px ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_type_section"
            ).value
          } ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_color_section"
            ).value
          }`
        );

      document
        .querySelector(".contact-divider-2")
        .style.setProperty(
          "--bannerBottom-border-bottom",
          `${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_size_section"
            ).value
          }px ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_type_section"
            ).value
          } ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_color_section"
            ).value
          }`
        );
    } else if (
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ) &&
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ).value === "top"
    ) {
      document
        .querySelector(".contact-divider-2")
        .style.setProperty(
          "--bannerBottom-border-top",
          `${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_size_section"
            ).value
          }px ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_type_section"
            ).value
          } ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_color_section"
            ).value
          }`
        );
    } else if (
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ) &&
      this.bottomBanner.find(
        (one) => one.key === "banner-bottom_border_position_section"
      ).value === "bottom"
    ) {
      document
        .querySelector(".contact-divider-2")
        .style.setProperty(
          "--bannerBottom-border-bottom",
          `${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_size_section"
            ).value
          }px ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_type_section"
            ).value
          } ${
            this.bottomBanner.find(
              (one) => one.key === "banner-bottom_border_color_section"
            ).value
          }`
        );
    }
  },
};
</script>

<style lang="scss">
.contact-divider-2 {
  background-color: rgb(245, 245, 245);
  padding: 0px;

  --bannerBottom-bg: #fff;
  --bannerBottom-fontSize: 20px;
  --bannerBottom-border-top: 0px solid #fff;
  --bannerBottom-border-bottom: 0px solid #fff;

  background: var(--bannerBottom-bg);
  border-top: var(--bannerBottom-border-top);
  border-bottom: var(--bannerBottom-border-bottom);
  background-repeat: no-repeat;
  background-size: cover;

  h3 {
    font-size: var(--steps-fontSize);
  }
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
  background-image: linear-gradient(
    270deg,
    rgba(0, 0, 0, 0) 50%,
    rgb(245, 245, 245) 100%
  );
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
.contact-divider-2 .btn i {
  margin-right: 12px;
}
.contact-divider-2 .btn:hover {
  border: none;
  background-color: rgb(40, 134, 89);
  color: #fff;
}
</style>
