<script>
import JumbotronPage from '../pages/JumbotronPage.vue';
import OffersPage from '../pages/OffersPage.vue';
export default {
  name: 'AppMain',
  components: {
    JumbotronPage,
    OffersPage
  }
}
</script>

<template>
    <div>
        <JumbotronPage></JumbotronPage>
        <OffersPage />
    </div>
</template>

<style scoped>

</style>