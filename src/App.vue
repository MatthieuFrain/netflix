<template>
<header>
  <div class="container">
    <img class="logo" src="./medias/Netflux-logo.png" alt="logo de netflux">
    <div class="nav-bar">
      <ul>
        <li><a href="#">Accueil</a></li>
        <li><a href="#">Séries</a></li>
        <li><a href="#">Films</a></li>
        <li><a href="#">Nouveautés les plus regardées</a></li>
        <li><a href="#">Ma liste</a></li>
      </ul>
  </div>
  </div>
</header>

       <video controls="true">
    <source src="./medias/SQUID-GAME.mp4" type="video/mp4" />
</video>
</template>

<script>


export default {
  name: 'App',
  components: {

  }
}
</script>

<style lang="css">

body{
  background-color: black;
}

.container{
    display: flex;
    margin-top: 20px;
    height: 41px;
    margin: 30px 60px;
}

.nav-bar,ul{
  display: flex;
  text-decoration: none;
}

.nav-bar a{
  color: white;
  text-decoration: none;
  padding: 30px;
  list-style: none;
}

.nav-bar,li{
  text-decoration: none;
}
</style>