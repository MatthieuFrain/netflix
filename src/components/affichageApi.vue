<template>
<div class="globalCategorie">
  <h3 class="titreCategorie">{{title}}</h3>
  <div class="contenuCategorie" v-for="result in post" :key="result">
    <div class="categorie">
      <b class="rank">{{result.rank}}</b>
      <img class="imgAffiche" :src="result.image">
      <br>
      <div>
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
    let url = "https://imdb-api.com/en/API/"+this.type+"/k_orp1gt36";
    axios
      .get(url)
      .then(response => (this.post = response.data.items))
  }
}
</script>

<style lang="css">
  .globalCategorie{
    color: white;
  }

  .imgAffiche{
    width: 150px;
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
</style>
