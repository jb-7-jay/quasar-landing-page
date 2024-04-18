<template>
  <q-layout view="lHr lpR fFf">
    <header-component />

    <q-page-container>
      <router-view />
    </q-page-container>

    <footer-component />
  </q-layout>
</template>

<script setup lang="ts">
import FooterComponent from './FooterComponent.vue';
import HeaderComponent from './HeaderComponent.vue';

defineOptions({
  name: 'MainLayout',
});
</script>
