<script>
import JumbotronPage from '../pages/JumbotronPage.vue';
import OffersPage from '../pages/OffersPage.vue';
//import MainGames from './MainGames.vue';
import axios from 'axios';
export default {
    name: 'AppMain',
    components: {
        JumbotronPage,
        OffersPage
        //MainGames
    },
    data() {
        return {
            games: []
        };
    },
    methods: {
        getGames() {
            axios.get('http://localhost:8000/api/games')
                .then(response => {
                    this.games = response.data.result;
                    console.log(response);
                });
        }
    },
    created() {
        this.getGames();
    }
}
</script>

<template>
    <JumbotronPage :games="games"></JumbotronPage>
    <OffersPage :games="games"></OffersPage>
    
</template>



<style lang="scss" scoped></style>