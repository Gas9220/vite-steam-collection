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
    <div id="offers" class="pb-3">
        <h3 class="container">OFFERTE SPECIALI</h3>
        <div class="container pb-5 justify-content-center d-flex">
            <div class="row">
                <div class="col-4" v-for="game in gamesFeature">
                    <img :src="game.thumbnail" :alt="game.title" class="image">
                    <div>
                        <span class="price p-2">{{ game.price === 0 ? 'Free to play' : game.price + '€'}}</span>
                        <span v-if="game.price != 0" class="discount p-2">-{{ game.discount }}%</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.price {
    background-color: #383f49;
    padding: 10px;
    color: #c2fb00;
    
}
.discount {
    background-color: #4b6c21;
    color: #bff517;
}
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