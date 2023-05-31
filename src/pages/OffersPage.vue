<script>
export default {
    name: 'OffersPage',
    props: {
        games: Object
    },
    computed: {
        gamesFeature() {
            const featuredGames = [...this.games];
            featuredGames.splice(0,2);
            return featuredGames;
        }
    },
    created() {
        console.log(this.games)
    }

}
</script>
<template>
    <div id="offers">
        <div class="container pb-5 justify-content-center d-flex">
            <div class="row">
                <div class="col-4" v-for="game in gamesFeature">
                    <img :src="game.thumbnail" :alt="game.title" class="placeholder image">
                    <div>
                        <span class="placeholder p-2">{{ game.price }}€</span>
                        <span class="placeholder p-2">{{ game.discount }}%</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
#offers {
    background-color: #0f1014;
}

h3 {
    color: white;
}

.placeholder {
    background-color: aqua;
    border: 1px solid;
}

.image {
    height: 200px;
    width: 12.5rem;
}
</style>