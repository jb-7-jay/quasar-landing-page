<template>
  <div class="gt-xs q-mt-xl">
    <transition
      appear
      enter-active-class="animated slower fadeIn"
      style="animation-delay: 500ms"
    >
      <swiper
        :autoplay="{
          delay: 5000,
          disableOnInteraction: false,
        }"
        :spaceBetween="30"
        :modules="modules"
        class="mySwiper"
        :breakpoints="{
          '440': {
            slidesPerView: 2.5,
          },
          '768': {
            slidesPerView: 3.5,
          },
          '1024': {
            slidesPerView: 4.5,
          },
        }"
      >
        <swiper-slide class="slide" v-for="index in 8" :key="index">
          <div class="logo-card">
            <img
              style="width: 32px; height: 32px"
              src="../../assets/timer.png"
              class="q-mr-md"
            />
            해외 마케팅 - {{ index }}
          </div>
        </swiper-slide>
      </swiper>
    </transition>
  </div>
</template>

<script lang="ts">
import 'swiper/css';
import { defineComponent } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Autoplay, Pagination, Navigation } from 'swiper/modules';

export default defineComponent({
  name: 'LogoSwiper',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation],
      isChecked: true,
    };
  },
});
</script>
