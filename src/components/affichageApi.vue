<template>
<h3 class="titreCategorie">{{title}}</h3>
<div class="globalCategorie">
  <div class="contenuCategorie" v-for="result in post" :key="result.id">
    <div class="categorie">
      <b class="rank">{{result.rank}}</b>
      <img class="imgAffiche" :src="result.image">
      <br>
      <div class='hover'>
        <b>{{result.title}}</b>
        <br>
        <b>{{result.imDbRating}} / 10</b>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'affichageApi',
  data() {
    return {
      post : []
    }
  },
  props: [
    "type",
    "title" 
  ],
  mounted(){
    const axios = require('axios').default;
    let url = "https://edu.maxence.space/imdb/"+this.type;
    axios
      .get(url)
      .then(response => (this.post = response.data.items))
  },
}
</script>

<style lang="css">
  .globalCategorie{
    color: white;
    display: flex;
    overflow-y: auto;
    position: relative;
  }

  .contenuCategorie{
    margin: 0 5px;
  }

  .imgAffiche{
    width: 150px;
    height: 230px;
  }

  .rank{
    position: absolute;
    background-color: black;
    font-size: 1.5em;
    padding: 10px;
    border-bottom-right-radius: 20px;
  }

  .categorie{
    position: relative;
  }

  .hover{
    position: absolute;
    top: 0;
    text-align: center;
    height: 100%;
    width: 100%;
    background-color: rgb(0 0 0 / 70%);
    visibility: hidden;
    cursor: pointer;
  }

  .imgAffiche:hover ~ .hover{
    visibility: visible;
    cursor: pointer;
    position: absolute;
    top: 0;
    text-align: center;
    height: 100%;
    width: 100%;
    background-color: rgb(0 0 0 / 70%);
  }

  .titreCategorie{
    color: white;
  }
</style>
