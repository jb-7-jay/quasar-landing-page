<template>
  <div>
    <transition
      appear
      enter-active-class="animated slower fadeIn"
      style="animation-delay: 500ms"
    >
      <swiper
        class="swiper"
        :modules="modules"
        :pagination="true"
        :effect="'coverflow'"
        :grab-cursor="true"
        :centered-slides="true"
        :navigation="true"
        :slides-per-view="'auto'"
        :coverflow-effect="{
          rotate: 0,
          stretch: 160,
          depth: 150,
          modifier: 1,
          slideShadows: true,
        }"
        :loop="true"
      >
        <swiper-slide class="slide" v-for="index in 8" :key="index">
          <!-- <div class="arrow">풀타임, 파트타임</div> -->

          <img
            style="width: 120px; height: 120px"
            src="../../assets/avatar.png"
          />
          <div class="name">
            {{ index % 2 === 0 ? 'Jolly Patel' : 'Adriana Lima' }}
          </div>
          <div class="experience">마케팅 · 2y+</div>

          <div class="description">
            <div class="text">마케팅 콘텐츠 제작</div>
            <div class="text">인스타그램 관리</div>
            <div class="row">
              <div class="text">트위터 관리</div>
              <div class="text q-mr-sm">블로그 글 작성</div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </transition>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { EffectCoverflow, Navigation } from 'swiper/modules';

import 'swiper/css';
import 'swiper/css/effect-coverflow';
import 'swiper/css/navigation';

export default defineComponent({
  name: 'ProfileSwiper',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [EffectCoverflow, Navigation],
    };
  },
});
</script>

<style lang="scss" scoped>
.swiper {
  height: 100%;
  width: 100%;
  padding-top: 50px;
  padding-bottom: 50px;

  .slide {
    max-width: 280px;
    width: 100%;

    background-color: white;
    color: black;
    border-radius: 10px;
    border: 1px solid transparent !important;
    padding: 30px 20px;

    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-direction: column;

    @media (max-width: $breakpoint-tablet) {
      width: 230px;
    }
  }

  .name {
    font-weight: 800;
    font-size: 22px;
    margin-top: 20px;
  }

  .experience {
    font-weight: 600;
    color: #4a77ff;
  }

  .text {
    border: 1px solid #c1c5cf;
    border-radius: 5px;
    padding: 4px 8px;
    display: inline-block;
  }

  .description {
    display: flex;
    flex-direction: column;
    gap: 5px;
    align-items: center;
    padding-top: 20px;
  }

  & .arrow {
    position: absolute;
    top: -50px;
    left: 32%;

    &::after {
      left: 45%;
    }
  }
}

.swiper-slide-shadow-coverflow {
  background-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0.2),
    rgba(0, 0, 0, 0) !important
  );
}
</style>
