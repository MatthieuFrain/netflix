<template>
<h3 class="titreCategorie">{{title}}</h3>
<div class="contenuCategorie" v-for="result in post" :key="result">
  <div class="categorie">
    <b>{{result.rank}}</b>
    <img :src="result.image">
    <b>{{result.title}}</b>
    <b>{{result.imDbRating}} / 10</b>
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

</style>
