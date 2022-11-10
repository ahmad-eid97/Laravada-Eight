<template>
  <section class="principles">
        <div class="row">
            <h2>Principles of our work</h2>
        </div>
        <div class="row">
            <div class="col-sm-6 col-lg-3 item">
                <span class="number">
                    01.
                </span>
                <h3>
                    Quality
                </h3>
                <p>
                    Nullam arcu felis, tristique eget malesuada sed, viverra at sapien. Maecenas gravida lacus nec dolor suscipit faucibus.
                </p>
            </div>
            <div class="col-sm-6 col-lg-3 item">
                <span class="number">
                    02.
                </span>
                <h3>
                    Quality
                </h3>
                <p>
                    Nullam arcu felis, tristique eget malesuada sed, viverra at sapien. Maecenas gravida lacus nec dolor suscipit faucibus.
                </p>
            </div>
            <div class="col-sm-6 col-lg-3 item">
                <span class="number">
                    03.
                </span>
                <h3>
                    Quality
                </h3>
                <p>
                    Nullam arcu felis, tristique eget malesuada sed, viverra at sapien. Maecenas gravida lacus nec dolor suscipit faucibus.
                </p>
            </div>
            <div class="col-sm-6 col-lg-3 item">
                <span class="number">
                    04.
                </span>
                <h3>
                    Quality
                </h3>
                <p>
                    Nullam arcu felis, tristique eget malesuada sed, viverra at sapien. Maecenas gravida lacus nec dolor suscipit faucibus.
                </p>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomePrinciples',
    data() {
        return {

        }
    }

}
</script>

<style lang="scss">
    .principles {
        padding: 90px 30px;
    }
    @include xs {
        .principles {
            text-align: center;
        }
    }
    .principles h2 {
        color: rgb(34, 34, 34);
        font-size: 36px;
        font-weight: 600;
        line-height: 43.2px;
        padding: 0 30px 30px;
        text-align: center;
    }
    .principles .item .number {
        color: rgb(48, 164, 108);
        font-size: 100px;
        font-weight: 100;
        line-height: 80px;
        word-spacing: 0px;
    }
    .principles .item h3 {
        margin-top: 30px;
        color: rgb(34, 34, 34);
        font-size: 22px;
        font-weight: 600;
        line-height: 28.6px;
    }
    .principles .item p {
        margin-top: 15px;
        color: rgb(34, 34, 34);
        color: rgb(102, 102, 102);
        font-size: 17px;
    }
</style>