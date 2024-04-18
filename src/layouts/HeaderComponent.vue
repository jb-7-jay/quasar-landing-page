<template>
  <q-header class="header bg-transparent">
    <div
      class="row items-center justify-between q-px-md"
      style="max-width: 1010px; width: 100%; margin: 0 auto; height: 60px"
    >
      <div class="row items-center justify-evenly">
        <img src="../assets/logo.svg" class="q-mr-sm" />
        <div class="text-weight-medium">hyperhire</div>
      </div>

      <div class="row items-center gt-xs">
        <q-select
          standout
          v-model="pageSelect"
          :options="options"
          bg-color="transparent"
        >
        </q-select>

        <div class="q-ml-md">해외 개발자 활용 서비스</div>
      </div>

      <q-btn
        color="white"
        text-color="black"
        label="문의하기"
        padding="xs lg"
        style="border-radius: 8px"
        class="gt-xs"
      />
    </div>
  </q-header>
</template>

<script setup>
import { ref } from 'vue';
const pageSelect = ref('채용');
const options = [
  '채용',
  '한국어 가능 외국인 채용',
  '외국인 원격 채용 (비개발 직군)',
  '해외 개발자 원격 채용',
];
// const options = ['employment', 'Hiring foreigners who can speak Korean', 'Remote recruitment of foreigners (non-development occupations)', 'Remote recruitment of overseas developers'];
</script>
