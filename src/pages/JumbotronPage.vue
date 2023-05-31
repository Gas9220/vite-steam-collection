<script>
import axios from 'axios';
export default {
  name: 'JumbotronPage',
  props:{
    data: Object
    }
}

</script>
<template>
    <div id="jumbotron">
        <div class="p-5">
        <!-- Nav Bar -->
        <nav id="nav" class="navbar navbar-expand-lg" data-bs-theme="dark">
            <div class="container-fluid">
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
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
                        <input id="search" class="form-control me-2" type="search" placeholder="cerca" aria-label="Search">

                    </form>
               </div>
            </div>
        </nav>
        <!-- / Nav Bar -->
        <!-- JUMBOTRON -->
        <h1 class="pt-3">GIOCHI</h1>
        <div class="container d-flex py-3 jumbo justify-content-center">
            <section class="col-4">
                <div>
                    <img src="#" alt="game.title" class="placeholder image">
                    <div class="price">
                        <span class="placeholder p-2">"Sconto"</span>
                        <span class="placeholder p-2">"Prezzo"</span>
                    </div>
                </div> 
            </section>
            <section class="col-6">
                <h2>game.title</h2>
                <div class="text">Data di rilascio: "DATE"</div>
                <div class="cont-genere">
                    <!-- aggiungere foreach here -->
                    <div class="p-1 me-1 placeholder">
                        Genere gioco
                    </div>
                    <div class="p-1 me-1 placeholder">
                        Genere gioco
                    </div>
                </div>
            </section>
        </div>
    </div>

    </div>
    
</template>

<style lang="scss" scoped>
.text{
    color:#d6cdce;
}
#jumbotron{
    background-color: #0f1014;
}
h1,h2{
    color: #f9f8f4;
}
#nav{
    background-color: #30638e;
}
#search{
    background-color: #316282;
    border: none;
}
.placeholder{
    background-color: aqua;
    border: 1px solid;
}
.image{
    height: 200px;
    width: 100%;
}
.price{
    position: relative;
    left: 55%;
    bottom: 50px;
}
// .jumbo{
// //     filter: blur(8px);

// }

</style>
