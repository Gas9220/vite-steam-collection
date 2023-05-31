<script>
export default {
  name: 'AppFooter'
}
</script>

<template>
  <footer>
    <div class="container">
      <hr>
      <div class="d-flex justify-content-between">
        <div>
          <img src="https://store.cloudflare.steamstatic.com/public/images/footerLogo_valve_new.png" alt="Valve Software">
        </div>
        <div>
          <img src="https://store.cloudflare.steamstatic.com/public/images/v6/logo_steam_footer.png" alt="Valve Software">
        </div>
      </div>
      <div class="text-center">
        <div>© 2023 Valve Corporation. Tutti i diritti riservati. Tutti i marchi appartengono ai rispettivi proprietari
          negli Stati Uniti e negli altri paesi.</div>
        <div>IVA inclusa nel prezzo (ove applicabile).&nbsp;&nbsp;

          <a href="#">Informativa sulla
            privacy</a>
          &nbsp; | &nbsp;
          <a href="#">Informazioni legali</a>
          &nbsp; | &nbsp;
          <a href="#">Contratto di sottoscrizione a Steam</a>
          &nbsp; | &nbsp;
          <a href="#">Rimborsi</a>
          &nbsp; | &nbsp;
          <a href="#">Cookie</a>
        </div>
        <hr>
      </div>

      <div class="text-center">
        <a href="#">Informazioni su Valve</a>
        &nbsp; | &nbsp;
        <a href="#">Impieghi</a>
        &nbsp; | &nbsp;
        <a href="#">Steamworks</a>
        &nbsp; | &nbsp;
        <a href="#">Distribuzione su Steam</a>
        &nbsp; | &nbsp;
        <a href="#">Assistenza</a>
        &nbsp; | &nbsp;
        <a href="#">Buoni regalo</a>
        &nbsp; | &nbsp;
        <a href="#"><img src="https://store.cloudflare.steamstatic.com/public/images/ico/ico_facebook.gif">Steam</a>
        &nbsp; | &nbsp;
        <a href="#"><img src="https://store.cloudflare.steamstatic.com/public/images/ico/ico_twitter.gif"> @steam</a>
      </div>
    </div>
  </footer>
</template>

<style scoped>
footer {
  background-color: #171a21;
  color: #7d8087;
  padding-top: 50px;
  padding-bottom: 30px;
}

a {
  text-decoration: none;
  color: #9d9fab;
}
</style>