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

      <video autoplay muted loop>
    <source src="./medias/squid.mp4" type="video/mp4" />
</video>
<div class="main-container">
    <h1>SQUID GAME</h1>
    <p>456 personnes, qui ont toutes des difficultés financières dans la vie, sont invitées à prendre part à une mystérieuse compétition de survie. Participant à une série de jeux traditionnels pour enfants, mais avec des issues mortelles, elles risquent leur vie pour gagner le prix de 45,6 milliards de wons (soit environ 38 millions de dollars américains ou 32 millions d'euros).</p>
    <button><a href="#">PLAY</a></button>
    <button class="button-right"><a href="#">INFOS</a></button>
</div>
<affichageApi title="TOP 100 - Films les plus populaires" type="mostpopular.json"/>

</template>

<script>
import affichageApi from './components/affichageApi.vue'

export default {
  name: 'App',
  components: {
    affichageApi
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

.nav-bar ul{
  display: flex;
  text-decoration: none;
}

.nav-bar a{
  color: white;
  text-decoration: none;
  padding: 30px;
}

.nav-bar li{
  list-style: none;
}

.nav-bar a:hover{
  font-weight:700;
  border-bottom: 0.6px solid #ffffff;
}

video {
/*  making the video fullscreen  */
  position: absolute;
  right: 0; 
  bottom: 0;
  min-width: 100%; 
  min-height: 100%;
  width: auto; 
  height: auto;
  z-index: -100;
}

.main-container h1{
  color: #ffffff;
  font-size: 50px;
}

.main-container p{
  color: #ffffff;
  width: 40%;
}

.main-container button{
  background-color: rgba(51,51,51,.6);
  border: none;
  color: #ffffff;
  padding: 12px 40px;
  font-size: 13px;
  font-weight: 600;
  display: inline-block;
  border-radius: 5px;
  -webkit-border-radius:5px;
  -moz-border-radius:5px;
  -ms-border-radius:5px;
  -o-border-radius:5px;
}

.main-container button:hover{
  background-color: rgba(255, 255, 255, 0.6);
}

.main-container a{
  text-decoration: none;
  color: #ffffff;
}

.button-right{
  margin-left: 20px;
}


</style>