<template>
  <section class="achievements">
    <div class="row m-0">
      <div class="col-lg-6 text">
        <h3>Our achievements</h3>
        <p>
          The ones who are crazy enough to think they can change the world, are
          the ones that do.
        </p>
        <div class="form">
          <div
            class="row m-0"
            v-if="
              counter.find((one) => one.key === 'counter_success_list').value
            "
          >
            <div
              v-for="item in counter.find(
                (one) => one.key === 'counter_success_list'
              ).value"
              :key="item"
              class="col-6 item"
              style="padding-left: 0"
            >
              <div class="row m-0">
                <div class="col-auto p-0 icono">
                  <i :class="item.icon"></i>
                </div>
                <div class="col" style="padding-left: 0">
                  <h4>{{ item.counter }}+</h4>
                  <p>{{ item.title }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-6 image">
        <div class="overlay"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeAchievements",
  props: ["counter"],
  components: {},
  data() {
    return {};
  },
  methods: {},
  mounted() {
    document
      .querySelector(".achievements")
      .style.setProperty(
        "--counter-bg",
        this.counter.find(
          (one) => one.key === "counter_success_background_active_section"
        ).value === "color"
          ? this.counter.find(
              (one) => one.key === "counter_success_background_color_section"
            ).value
          : `url(${
              this.counter.find(
                (one) => one.key === "counter_success_background_image_section"
              ).value
            })`
      );

    document
      .querySelector(".achievements")
      .style.setProperty(
        "--counter-fontSize",
        `${
          this.counter.find(
            (one) => one.key === "counter_success_font_size_section"
          ).value
        }px`
      );

    if (
      this.counter.find(
        (one) => one.key === "counter_success_border_position_section"
      ) &&
      this.counter.find(
        (one) => one.key === "counter_success_border_position_section"
      ).value === "both"
    ) {
      document
        .querySelector(".achievements")
        .style.setProperty(
          "--counter-border-top",
          `${
            this.counter.find(
              (one) => one.key === "counter_success_border_size_section"
            ).value
          }px ${
            this.counter.find(
              (one) => one.key === "counter_success_border_type_section"
            ).value
          } ${
            this.counter.find(
              (one) => one.key === "counter_success_border_color_section"
            ).value
          }`
        );

      document
        .querySelector(".achievements")
        .style.setProperty(
          "--counter-border-bottom",
          `${
            this.counter.find(
              (one) => one.key === "counter_success_border_size_section"
            ).value
          }px ${
            this.counter.find(
              (one) => one.key === "counter_success_border_type_section"
            ).value
          } ${
            this.counter.find(
              (one) => one.key === "counter_success_border_color_section"
            ).value
          }`
        );
    } else if (
      this.counter.find(
        (one) => one.key === "counter_success_border_position_section"
      ) &&
      this.counter.find(
        (one) => one.key === "counter_success_border_position_section"
      ).value === "top"
    ) {
      document
        .querySelector(".achievements")
        .style.setProperty(
          "--counter-border-top",
          `${
            this.counter.find(
              (one) => one.key === "counter_success_border_size_section"
            ).value
          }px ${
            this.counter.find(
              (one) => one.key === "counter_success_border_type_section"
            ).value
          } ${
            this.counter.find(
              (one) => one.key === "counter_success_border_color_section"
            ).value
          }`
        );
    } else if (
      this.counter.find(
        (one) => one.key === "counter_success_border_position_section"
      ) &&
      this.counter.find(
        (one) => one.key === "counter_success_border_position_section"
      ).value === "bottom"
    ) {
      document
        .querySelector(".achievements")
        .style.setProperty(
          "--counter-border-bottom",
          `${
            this.counter.find(
              (one) => one.key === "counter_success_border_size_section"
            ).value
          }px ${
            this.counter.find(
              (one) => one.key === "counter_success_border_type_section"
            ).value
          } ${
            this.counter.find(
              (one) => one.key === "counter_success_border_color_section"
            ).value
          }`
        );
    }
  },
};
</script>

<style lang="scss">
.achievements {
  background-color: rgb(245, 245, 245);

  --counter-bg: #fff;
  --counter-fontSize: 20px;
  --counter-border-top: 0px solid #fff;
  --counter-border-bottom: 0px solid #fff;

  background: var(--counter-bg);
  border-top: var(--counter-border-top);
  border-bottom: var(--counter-border-bottom);
  background-repeat: no-repeat;
  background-size: cover;
  h2 {
    font-size: var(--counter-fontSize);
  }
}
.achievements .image {
  background-image: url("https://the7.io/elementor-business/wp-content/uploads/sites/89/2020/02/img001-5-1.jpg");
  position: relative;
  background-position-x: 50%;
  background-position-y: 50%;
  background-size: cover;
  box-sizing: border-box;
  min-height: 400px;
}
.achievements .image .overlay {
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
.achievements .text {
  padding: 120px 60px;
}
@include md {
  .achievements .text {
    padding: 50px 40px;
  }
}
.achievements .text h3 {
  color: rgb(34, 34, 34);
  font-size: 28px;
  font-weight: 600;
  line-height: 36.4px;
  margin-bottom: 30px;
}
.achievements .text p {
  color: rgb(102, 102, 102);
  font-size: 19px;
  margin-bottom: 30px;
}
.achievements label {
  box-sizing: border-box;
  color: rgb(34, 34, 34);
  font-size: 17px;
  padding-bottom: 5px;
}
.achievements input {
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
.achievements input:focus {
  box-shadow: none;
  border-color: var(--main-color);
}
.achievements .btn {
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
.icono i {
  margin-top: 20px !important;
}
.achievements .btn i {
  margin-right: 12px;
}
.achievements .btn:hover {
  border: none;
  background-color: rgb(40, 134, 89);
  color: #fff;
}
.achievements .item i {
  color: rgb(48, 164, 108);
  display: block;
  font-size: 32px;
  font-weight: 400;
  height: 32px;
  line-height: 32px;
  padding: 4.8px;
  margin-right: 20px;
}
.achievements .item h4 {
  color: rgb(34, 34, 34);
  font-size: 36px;
  font-weight: 600;
  line-height: 43.2px;
  text-align: left;
}
.achievements .item p {
  color: rgb(34, 34, 34);
  font-size: 19px;
  font-weight: 600;
  margin-top: 10px;
  text-align: left;
}
</style>
