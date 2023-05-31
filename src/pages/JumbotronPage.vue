<script>
export default {
    name: 'JumbotronPage',
    props: {
        games: Object
    },
    methods: { //Take time and return a different format with 3 letters month and D-M-Y format
        formatDate(dateString) {
            const date = new Date(dateString);
            const day = date.getDate();
            const year = date.getFullYear();
            const month = date.toLocaleString('it-IT', { month: 'short' });

            return `${day} ${month} ${year}`;
        }
    }
}

</script>
<template>
    <div id="jumbotron">
        <div class="p-5 position-relative">
            <img class="bg-img" :src="games[0].thumbnail" alt="">
            <!-- Nav Bar -->
            <nav id="nav" class="navbar navbar-expand-lg" data-bs-theme="dark">
                <div class="container-fluid">
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                        data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent"
                        aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                    <div class="collapse navbar-collapse" id="navbarSupportedContent">
                        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                            <li class="nav-item">
                                <a class="nav-link active">Il tuo Negozio</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active">Novita e tendenze</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active">Categorie</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active">Negozio dei Punti</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active">Notizie</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link active">Laboratori</a>
                            </li>
                        </ul>
                        <form class="d-flex" role="search">
                            <input id="search" class="form-control me-2" type="search" placeholder="cerca"
                                aria-label="Search">

                        </form>
                    </div>
                </div>
            </nav>
            <!-- / Nav Bar -->
            <!-- JUMBOTRON -->
            <h1 class="pt-3">GIOCHI</h1>
            <div class="container d-flex py-3 jumbo justify-content-center z-2">
                <div class="row gap-5">
                    <div class="col-4">
                        <div v-if="games[0]">
                            <img :src="games[0].thumbnail" :alt="games[0].title" class="image">
                            <div class="price">
                                <span class="p-2 discount">-{{ games[0].discount }}%</span>
                                <span class="p-2 price-style">{{ games[0].price }}€</span>
                            </div>
                        </div>
                    </div>
                    <div class="col-6" v-if="games[0]">
                        <h2>{{ games[0].title }}</h2>
                        <div class="text">Data di rilascio:  {{ formatDate(games[0].publication_year) }}</div>
                        <div class="cont-genere d-flex">
                            <!-- aggiungere foreach here -->

                            <div class="genre-tag p-1 rounded mt-2" v-for="genre in games[0].genres">
                                <span class="text-white">{{ genre.name }}</span>
                            </div>
                        </div>
                    </div>
                </div>
                <section class="col-4">

                </section>

            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
.price-style {
    background-color: #383f49;
    color: #c2fb00;
}

.bg-img {
    position: absolute;
    left: 50%;
    top: 50%;
    object-fit: fill;
    transform: translate(-50%, -50%);
    opacity: 0.2;
}

.discount {
    background-color: #4b6c21;
    color: #bff517;
}

.text {
    color: #d6cdce;
}

.genre-tag {
    background-color: rgba($color: #909090, $alpha: 0.3);
}

#jumbotron {
    background-color: #0f1014;
}

h1,
h2 {
    color: #f9f8f4;
}

#nav {
    background-color: #30638e;
}

#search {
    background-color: #316282;
    border: none;
}

.placeholder {
    background-color: aqua;
    border: 1px solid;
}

.image {
    height: 200px;
    width: 100%;
}

.price {
    position: relative;
    left: 55%;
    bottom: 50px;
}

// .jumbo{
// //     filter: blur(8px);

// }</style>
