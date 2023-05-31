<script>
export default {
    name: 'MainGames',
    props: {
        games: Array
    },
    methods: { //Take time and return a different format with 3 letters month and D-M-Y format
        formatDate(dateString) {
            const date = new Date(dateString);
            const day = date.getDate();
            const year = date.getFullYear();
            const month = date.toLocaleString('it-IT', { month: 'short' }).toUpperCase();

            return `${day} ${month} ${year}`;
        }
    }
}
</script>

<template>
    <div class="games-container">
        <h2 class="title">I GIOCHI</h2>
        <div v-for="game in  games" class="games shadow-lg mb-2">
            <div class="col-12 d-flex">
                <div class="img"><img
                        :src="game.thumbnail"
                        :alt="game.title"></div>
                <div class="games-info d-flex justify-content-between w-100">
                    <div>
                        <h2 class="games-title text-uppercase">{{ game.title }}</h2>
                        <div v-for="genre in genres" :key="genre.id" class="d-flex">
                            <div class="tag">{{ genre }}</div>
                        </div>
                        <div class="d-flex">
                            <div class="date">{{ formatDate(game.publication_year) }}</div>
                            <i class="fa-solid fa-laptop"></i>
                        </div>
                    </div>
                    <div class="d-flex price-tags align-self-end shadow">
                        <h2 class="discount" v-if="game.discount !== 0">{{ game.discount }}%</h2>
                        <div class="price">
                            <h5 class="old-price" v-if="game.price !== 0"
                                :style="game.discount !== 0 ? 'text-decoration: line-through' : 'color: #b1b9c4'">{{
                                    game.price }}€</h5>
                            <h5 class="old-price" v-else style="color: #b1b9c4">Free-to-Play</h5>
                            <h4 class="new-price" v-if="game.discount !== 0 && game.price !== 0">{{ game.price - (game.price

                                (game.discount / 100)) }}€</h4>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css%22%3E">
</template>

<style lang="scss" scoped>
//RESET
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

//TITLE
.tag {
    margin-top: 10px;
    padding: 5px;
    padding: 0px 8px;
    color: #9a9fa8;
}

.games-container {
    padding-bottom: 40px;
}

.date {
    color: #9a9fa8;
    font-weight: 500;
    font-size: 20px;
    margin-right: 10px;
}

.games {
    padding-bottom: 5px;
    margin: 0 auto;
    max-width: 1100px;
}

h3 {
    color: #f2f4f8;
}

img {
    height: 200px;
    object-fit:contain;
    margin-right: 15px;
    padding: 5px;
}

.games-title {
    color: #c0c6cf;
}

.title {
    color: white;
    padding: 20px 100px 50px 0px;
    font-weight: 300;
}

.old-price {
    color: #626d73;
}

.price {
    background-color: #383f49;
    padding: 10px;
}

.tag {
    background-color: #49525d;
}

.discount {
    padding: 10px;
    align-items: center;
}

.games-container {
    background-color: #4b5b6a;
    padding: 0px 90px;
    padding-bottom: 110px;
}

.discount {
    background-color: #4b6c21;
    color: #bff517;
}

.games {
    background-color: #404954;
}

.games-info {
    margin: 15px 10px;
}

.price-tags {
    margin: 0px 5px;
}

.new-price {
    background-color: #232e26;
    color: #b1d43b;
}
</style>