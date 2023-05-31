<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppMainVue from './components/AppMain.vue';
export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
    AppMainVue
  }
}
</script>

<template>
  <AppHeader />
  <AppMainVue />
  <AppFooter />
</template>

<style scoped></style>
