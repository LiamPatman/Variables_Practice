<template>
<!-- <span @click="data_fetch">LOAD</span> -->
<h3 v-for='news_article in my_data_array'>{{news_article.title}}</h3>
</template>
<script>
export default {
  data(){ // data itself starts
    return{ // data variables starts
      my_data_array:[]
    } // data variables end
  }, // data itself ends
  methods:{ // funtions are written in methods
    async data_fetch(){
      const response = await fetch("https://newsapi.org/v2/everything?q=tesla&apiKey=ffd711aad23843739f3a3c42ff9b8f7d");
      const received_data = await response.json();
      // at this point our data is available under received_data variable
      
      this.my_data_array = received_data.articles;

      console.log( this.my_data_array[0] );
    }
  }, // methods end
  created(){ // created() is where initial code runs once
    this.data_fetch();
  } // end of created
}
</script>
<style>
</style>