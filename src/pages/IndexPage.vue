<template>
  <q-page class="hero-banner-container">
    <div class="hero-banner">
      <div class="hero-banner-two-sections">
        <div class="hero-left-section">
          <transition
            appear
            enter-active-class="animated fadeIn"
            style="animation-delay: 500ms"
          >
            <div class="arrow">풀타임, 파트타임</div>
          </transition>

          <transition-group
            appear
            enter-active-class="animated slower fadeInUp"
            style="animation-duration: 800ms"
          >
            <h4 key="text" class="text-weight-bolder q-my-md">
              최고의 실력을 가진 <br />
              외국인 인재를 찾고 계신가요?
            </h4>

            <div key="text-1" class="text-weight-bolder">
              <div>법률 및 인사관리 부담없이</div>
              <div>1주일 이내에 원격으로 채용해보세요.</div>
              <div
                class="q-pt-md text-weight-bold gt-xs"
                style="border-bottom: 1px solid white; display: inline-block"
              >
                발자가 필요하신가요?
              </div>
            </div>
          </transition-group>

          <transition-group
            appear
            enter-active-class="animated slower fadeIn"
            style="animation-duration: 800ms"
          >
            <div key="test" class="left-section-footer gt-xs">
              <div class="card">
                <div class="text-weight-bolder">평균 월 120만원</div>
                <div class="q-mt-sm">
                  임금을 해당 국가를 기준으로 계산합니다.
                </div>
              </div>
              <div class="card">
                <div class="text-weight-bolder">최대 3회 인력교체</div>
                <div class="q-mt-sm">
                  막상 채용해보니 맞지 않아도 걱정하지 마세요.
                </div>
              </div>
              <div class="card">
                <div class="text-weight-bolder">평균 3일, 최대 10일</div>
                <div class="q-mt-sm">
                  급하게 사람이 필요한 경우에도 빠른 채용이 가능합니다.
                </div>
              </div>
            </div>
          </transition-group>
        </div>

        <div class="hero-right-section">
          <profile-swiper />
        </div>
      </div>

      <logo-swiper />

      <div class="lt-sm q-pl-md">
        <div class="row">
          <div class="row items-center q-pr-md">
            <q-checkbox v-model:model-value="isChecked" class="q-pr-sm" />
            겸업 여부
          </div>
          <div class="row items-center">
            <q-checkbox v-model:model-value="isChecked" />
            업무 수행 능력
          </div>
        </div>
        <div class="row">
          <div class="row items-center q-pr-md">
            <q-checkbox v-model:model-value="isChecked" class="q-pr-sm" />
            겸업 여부
          </div>
          <div class="row items-center">
            <q-checkbox v-model:model-value="isChecked" />
            평판 조회
          </div>
        </div>

        <a class="link">발자가 필요하신가요?</a>
      </div>
    </div>
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { Autoplay, Pagination, Navigation } from 'swiper/modules';

import LogoSwiper from 'src/components/home/LogoSwiper.vue';
import ProfileSwiper from 'src/components/home/ProfileSwiper.vue';

import 'swiper/css';

export default defineComponent({
  name: 'IndexPage',
  components: {
    ProfileSwiper,
    LogoSwiper,
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation],
      isChecked: true,
    };
  },
});
</script>

<style lang="scss" scoped>
.logo-card {
  display: flex;
  align-items: center;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 5px;
  font-weight: 700;
  font-size: 18px;
  padding: 15px;
}

a {
  color: #fbff23;
  font-size: 16px;
  font-weight: 900;
  margin-top: 10px;
  padding-bottom: 30px;
  display: inline-block;
}
</style>
