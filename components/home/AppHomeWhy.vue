<template>
  <section class="testimonials">
    <div class="row mb-3">
      <h2>
        {{ whyUs.find((one) => one.key === "why_choose_us_title").value }}
      </h2>
    </div>
    <div class="row">
      <div class="col-lg-8">
        <div
          class="row m-0 h-100"
          v-if="whyUs.find((one) => one.key === 'why_choose_us_list').value"
        >
          <div
            v-for="item in whyUs.find((one) => one.key === 'why_choose_us_list')
              .value"
            :key="item"
            class="col-md-6 item"
          >
            <i :class="item.icon"></i>
            <h4>{{ item.title }}</h4>
            <p>
              {{ item.description }}
            </p>
          </div>
        </div>
      </div>
      <div class="col-lg-4" v-for="member in team" :key="member.id">
        <div class="founder">
          <div class="image">
            <img :src="member.image" alt="member image" />
          </div>
          <p>
            {{ member.description.substring(0, 200) }}
            {{ member.description.length > 200 ? "..." : "" }}
          </p>
          <h4>{{ member.name }}</h4>
          <h5>{{ member.job }}</h5>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHometestimonials",
  props: ["whyUs", "team"],
  components: {},
  data() {
    return {
      show: "show1",
    };
  },
  mounted() {
    this.autoPlay();
    document
      .querySelector(".testimonials")
      .style.setProperty(
        "--steps-bg",
        this.whyUs.find(
          (one) => one.key === "why_choose_us_background_active_section"
        ).value === "color"
          ? this.whyUs.find(
              (one) => one.key === "why_choose_us_background_color_section"
            ).value
          : `url(${
              this.whyUs.find(
                (one) => one.key === "why_choose_us_background_image_section"
              ).value
            })`
      );

    document
      .querySelector(".testimonials")
      .style.setProperty(
        "--steps-fontSize",
        `${
          this.whyUs.find(
            (one) => one.key === "why_choose_us_font_size_section"
          ).value
        }px`
      );

    if (
      this.whyUs.find(
        (one) => one.key === "why_choose_us_border_position_section"
      ) &&
      this.whyUs.find(
        (one) => one.key === "why_choose_us_border_position_section"
      ).value === "both"
    ) {
      document
        .querySelector(".testimonials")
        .style.setProperty(
          "--steps-border-top",
          `${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_size_section"
            ).value
          }px ${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_type_section"
            ).value
          } ${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_color_section"
            ).value
          }`
        );

      document
        .querySelector(".testimonials")
        .style.setProperty(
          "--steps-border-bottom",
          `${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_size_section"
            ).value
          }px ${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_type_section"
            ).value
          } ${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_color_section"
            ).value
          }`
        );
    } else if (
      this.whyUs.find(
        (one) => one.key === "why_choose_us_border_position_section"
      ) &&
      this.whyUs.find(
        (one) => one.key === "why_choose_us_border_position_section"
      ).value === "top"
    ) {
      document
        .querySelector(".testimonials")
        .style.setProperty(
          "--steps-border-top",
          `${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_size_section"
            ).value
          }px ${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_type_section"
            ).value
          } ${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_color_section"
            ).value
          }`
        );
    } else if (
      this.whyUs.find(
        (one) => one.key === "why_choose_us_border_position_section"
      ) &&
      this.whyUs.find(
        (one) => one.key === "why_choose_us_border_position_section"
      ).value === "bottom"
    ) {
      document
        .querySelector(".testimonials")
        .style.setProperty(
          "--steps-border-bottom",
          `${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_size_section"
            ).value
          }px ${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_type_section"
            ).value
          } ${
            this.whyUs.find(
              (one) => one.key === "why_choose_us_border_color_section"
            ).value
          }`
        );
    }
  },
  methods: {
    autoPlay() {
      var items = ["show1", "show2", "show3", "show4", "show5"];
      var item = "";
      let _this = this;
      setInterval(function () {
        item = items[Math.floor(Math.random() * items.length)];
        _this.showData(item);
      }, 5000);
    },
    showData(show) {
      this.show = show;
    },
  },
};
</script>

<style lang="scss">
.testimonials {
  padding: 90px 30px;
  --steps-bg: #fff;
  --steps-fontSize: 20px;
  --steps-border-top: 0px solid #fff;
  --steps-border-bottom: 0px solid #fff;

  background: var(--steps-bg);
  border-top: var(--steps-border-top);
  border-bottom: var(--steps-border-bottom);
  background-repeat: no-repeat;
  background-size: cover;
  padding: 50px 0 0 0;

  h2 {
    font-size: var(--steps-fontSize);
    text-align: center;
  }
}
.testimonials h2 {
  color: rgb(34, 34, 34);
  font-size: 36px;
  font-weight: 600;
  line-height: 43.2px;
  padding: 0 30px 30px;
  text-align: center;
}
.testimonials .item .number {
  color: rgb(48, 164, 108);
  font-size: 100px;
  font-weight: 100;
  line-height: 80px;
  word-spacing: 0px;
}
.testimonials .item h3 {
  margin-top: 30px;
  color: rgb(34, 34, 34);
  font-size: 22px;
  font-weight: 600;
  line-height: 28.6px;
}
.testimonials .item p {
  margin-top: 15px;
  color: rgb(34, 34, 34);
  color: rgb(102, 102, 102);
  font-size: 17px;
}
.testimonials .founder {
  color: rgb(102, 102, 102);
  font-size: 17px;
  padding-bottom: 40px;
  padding-left: 30px;
  padding-right: 30px;
  padding-top: 40px;
  /* width: 342.6px; */
  background-color: rgb(245, 245, 245);
}
.testimonials .founder .image {
  text-align: center;
  margin-bottom: 30px;
}
.testimonials .founder .image img {
  width: 141px;
  height: 141px;
  border-radius: 50%;
  margin: 0 auto;
}
.testimonials .founder p {
  color: rgb(102, 102, 102);
  font-size: 19px;
  line-height: 30.4px;
  text-align: center;
  margin-bottom: 20px;
}
.testimonials .founder h4 {
  color: rgb(34, 34, 34);
  font-size: 19px;
  font-weight: 600;
  line-height: 26.6px;
  text-align: center;
  margin-bottom: 10px;
}
.testimonials .founder h5 {
  color: rgb(48, 164, 108);
  font-size: 17px;
  font-weight: 400;
  line-height: 27.2px;
  text-align: center;
}
.testimonials .item i {
  color: rgb(48, 164, 108);
  display: block;
  font-size: 32px;
  font-weight: 900;
  height: 32px;
  line-height: 32px;
  margin-bottom: 20px;
  position: relative;
  text-align: center;
  width: 32px;
}
.testimonials .item h4 {
  color: rgb(34, 34, 34);
  font-size: 22px;
  font-weight: 600;
  line-height: 28.6px;
  /* text-align: left; */
}
.testimonials .item p {
  color: rgb(102, 102, 102);
  font-size: 17px;
  font-weight: 400;
  line-height: 27.2px;
  margin-top: 15px;
  /* text-align: left; */
}
</style>
