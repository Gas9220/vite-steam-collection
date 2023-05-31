<script>
import MainGames from './MainGames.vue';
import axios from 'axios';
export default {
    name: 'AppMain',
    components: {
        MainGames
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
        },
    },
    created() {
        this.getGames();
    }
}
</script>

<template>
    <MainGames :games="games"></MainGames>
</template>



<style lang="scss" scoped></style>