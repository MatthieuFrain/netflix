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
  align-content: center;
  margin-top: 20px;
}
.logo{
  width: 120px;
  margin-left: 100px;

}
.nav-bar,ul{
  display: flex;

}
</style>