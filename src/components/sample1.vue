<template>
  <!-- all HTML content -->
  <!-- other components also are used in template area-->
  <!-- Here some examples for using it as innerHTML -->
  <h1>This is plain text in h1</h1>
  <h2>{{ myMessage }}</h2>
  <h2>Plain text combined with variable value {{ myMessage }}</h2>
  <!-- here is how we combine it inside a message -->
  <h3>Price is : {{ price }}$</h3>
  <!-- v-if is the way we can do display:none depending on a boolean -->
  <p v-if="myBoolean">This message displays only if myBoolean is true</p>
  <!-- we can provide a variable as property to a html (such as class, src, href etc) -->
  <!-- the way to do it is by writing v-bind: before the property, 
  but since it is used often a shorter version was introduced later as just : -->
  <!-- we can use regular class and v-bind:class together in same element -->
  <span v-bind:class="myColor" class="bordered">colored</span> 
  <span :class="myColor">colored</span>
  <!-- here is a different way of doing something similar, below item wil have a normal CSS class 
  but that class will have a binded value -->
  <span class="binded-color">colored</span>
  <!-- we can also v-bind: img src from a variable -->
  <img :src="imgUrl" alt="">

</template>
<style scoped>
  /* all CSS classes are defined here */
  .red{color: red;}
  .blue{color: blue;}
  .bordered{border: 1px solid black;}
  .binded-color{
    color: v-bind(myColor);
  }
</style>
<script setup>
  // all imports for other components are done in setup
  // Prop declarations also are done in script setup
</script>
<script>
export default {
  data(){
    return{ // data Start
      myMessage : 'Hello World',
      price : 10,
      myBoolean : true,
      myColor : 'blue',
      imgUrl : 'https://media.sproutsocial.com/uploads/2017/02/10x-featured-social-media-image-size.png'

      
    } // data End
  }
}
</script>