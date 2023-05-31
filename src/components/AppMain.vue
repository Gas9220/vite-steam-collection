<script>
import JumbotronPage from '../pages/JumbotronPage.vue';
import axios from 'axios';
export default {
    name: 'AppMain',
    components: {
        JumbotronPage
    }
}
</script>

<template>
  <JumbotronPage :games="games"></JumbotronPage>
</template>



<style lang="scss" scoped></style>