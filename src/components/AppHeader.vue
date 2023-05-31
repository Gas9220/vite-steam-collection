<script>
export default {
  name: 'AppHeader'
}
</script>

<template>
  <header class="container-fluid">
    <div class="container d-flex justify-content-between">
      <div class="my-container d-flex">
        <nav class="navbar navbar-expand-lg">
          <img src="https://store.cloudflare.steamstatic.com/public/shared/images/header/logo_steam.svg?t=962016"
            width="176" height="44">
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          </button>

          <div class="d-flex gap-4 text-uppercase">
            <a class="nav-link active" aria-current="page" href="#">Negozio</a>

            <a class="nav-link active" aria-current="page" href="#">Comunità</a>

            <a class="nav-link active" aria-current="page" href="#">Informazioni</a>
            <a class="nav-link active" aria-current="page" href="#">Assistenza</a>
          </div>
        </nav>
      </div>

      <div class="">
        <nav class="navbar navbar-expand-lg gap-1 my-box">

          <button><i class="bi bi-download pe-2"></i>Installa Steam</button>

          <a class="nav-link active " aria-current="page" href="#">Accedi</a>

          &nbsp; | &nbsp;

          <div class="dropdown d-flex">
            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              Lingua
            </a>
            <ul class="dropdown-menu my-dropdown">
              <li><a class="dropdown-item" href="#">Italiano</a></li>
              <li><a class="dropdown-item" href="#">English (inglese)</a></li>
              <li><a class="dropdown-item" href="#">Español (spagnolo)</a></li>
              <li><a class="dropdown-item" href="#">Français (francese)</a></li>
              <li><a class="dropdown-item" href="#">繁體中文 (cinese tradizionale)</a></li>
              <li><a class="dropdown-item" href="#">Русский (russo)</a></li>
              <li><a class="dropdown-item" href="#">Tiếng Việt (vietnamita)</a></li>
              <li><a class="dropdown-item" href="#">日本語 (giapponese)</a></li>
              
            </ul>
          </div>
        </nav>
      </div>
    </div>
  </header>
</template>

<style scoped>
header, .my-dropdown {
  background-color: #171a21;
  color: #c3c3b9;
}

.my-container {
  height: 8.125rem;
}

button {
  padding: 0 20px;
  background-color: #60830b;
  color: white;
}
a{
  color: #c3c3b9;
}
</style>