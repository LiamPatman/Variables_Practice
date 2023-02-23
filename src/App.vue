<script setup>
  import HeaderComponent from './components/Header.vue'
  import SearchComponent from './components/SearchBar.vue'
  import NewsArticleComponent from './components/NewsArticle.vue';
</script>

<template>
<!-- <span @click="data_fetch">LOAD</span> -->
  <HeaderComponent />
  <SearchComponent />
  <NewsArticleComponent />
  
  <!-- <div class="article" v-for='news_article in my_data_array'>
    <h1>{{news_article.title}}</h1>
    <h2>{{news_article.author}}</h2>
    <h3>{{news_article.description}}</h3>
  </div> -->

</template>


<script>
// export default {
//   data(){ // data itself starts
//     return{ // data variables starts
//       my_data_array:[]
//     } // data variables end
//   }, // data itself ends
//   methods:{ // funtions are written in methods
//     async data_fetch(){
//       const response = await fetch("https://newsapi.org/v2/everything?q=tesla&apiKey=ffd711aad23843739f3a3c42ff9b8f7d");
//       const received_data = await response.json();
//       // at this point our data is available under received_data variable
      
//       this.my_data_array = received_data.articles;

//       console.log( this.my_data_array[0] );
//     }
//   }, // methods end
//   created(){ // created() is where initial code runs once
//     this.data_fetch();
//   } // end of created
// }
</script>


<style>
  
</style>