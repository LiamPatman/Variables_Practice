<template>
  <!-- we add interaction via @click=" " -->
  <!-- inside @click=" " we either write a JS line of code directly or we write a function's name-->
  <h1 @click="myboolean = !myboolean;">Reverse 'myboolean' value</h1>
  <!-- any item that relies on the value of changed variable updates automatically -->
  <span>{{myboolean}}</span>
  <h2 :class="{bordered:myboolean}">bordered on condition</h2>
  <h2 v-if="myboolean">reveal on myboolean</h2>
  <h3 :class="{blue:myboolean}">OooOOoooOoOh so blueeee</h3>
  <h3 v-if="myboolean">Why hello there</h3>
</template>
<script>
export default {
  data(){ // data itself starts
    return{ // data variables starts
      myboolean : false
    } // data variables end
  }
}
</script>
<style>
h1{
  background-color: rgb(222, 170, 103);
  padding: 10px;
  border-radius: 10px;
  border: 1px solid black;
}
.bordered{border: 1px solid black;}
.blue{
  color: blue;
}
</style>