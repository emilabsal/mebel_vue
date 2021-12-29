<template>
  <div class="banner container">
    <swiper
      :slides-per-view="1"
      :space-between="0"
      :navigation="true"
      swiper.navigation.nextEl=".swiper-button-next"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      class="swiper-cards"
    >
      <swiper-slide>
        <div class="card">
          <img src="@/assets/slides/img1.png" alt="banner" />
          <div class="card-desc">
            <h3>Финальная распродажа</h3>
            <p>Только 30 моделей можно забрать домой со скидкой до 45%</p>
            <a href="#">Подробнее</a>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="@/assets/slides/img1.png" alt="banner" />
          <div class="card-desc">
            <h3>Финальная распродажа</h3>
            <p>Только 30 моделей можно забрать домой со скидкой до 45%</p>
            <a href="#">Подробнее</a>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="@/assets/slides/img1.png" alt="banner" />
          <div class="card-desc">
            <h3>Финальная распродажа</h3>
            <p>Только 30 моделей можно забрать домой со скидкой до 45%</p>
            <a href="#">Подробнее</a>
          </div>
        </div>
      </swiper-slide>
    </swiper>
    <div class="banner-right">
      <img src="@/assets/slides/img1.png" alt="banner" />
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/swiper-bundle.min.css";
import "swiper/swiper.min.css";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      slides: [
        { id: 1, img: "@/assets/slides/img1.png" },
        { id: 2, img: "@/assets/slides/img1.png" },
        { id: 3, img: "@/assets/slides/img1.png" },
      ],
    };
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };

    return {
      onSwiper,
      onSlideChange,
    };
  },
};
</script>

<style lang="scss" scoped>
.banner {
  margin-top: 40px;
  display: flex;
  gap: 46px;
  overflow: hidden;
  width: 100%;
}

.swiper-cards {
  width: 80%;
  border-radius: 8px;
}

.banner-right {
  width: 20%;
  overflow: hidden;

  img {
    object-fit: cover;
    object-position: right;
  }
}

.card {
  width: 100%;
  height: 100%;
  position: relative;
  z-index: 1;
  display: flex;
  align-items: center;
  justify-content: flex-start;

  img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
  }

  &-desc {
    padding-left: 70px;
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
    flex-direction: column;
    max-width: 500px;

    h3 {
      font-size: 64px;
      font-weight: 700;
      line-height: 87.16px;
      text-align: left;
      margin-bottom: 22px;
    }

    p {
      font-weight: 600;
      font-size: 24px;
      line-height: 33px;
      text-align: left;
      margin-bottom: 32px;
    }

    a {
      display: inline-block;
      padding: 10px 25px;
      border: 1px solid $darkColor;
      border-radius: 8px;
      font-weight: 600;
      font-size: 18px;
      line-height: 24.51px;
      text-decoration: none;
    }
  }
}

.swiper-button-next {
  background: #fff;
  width: 65px;
  height: 65px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>