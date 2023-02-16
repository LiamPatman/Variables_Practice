<template>
  <!-- we add interaction via @click=" " -->
  <!-- inside @click=" " we either write a JS line of code directly or we write a function's name-->
  <h1 @click="mybool_reverse">Reverse 'myboolean' value</h1>
  <!-- any item that relies on the value of changed variable updates automatically -->
  <span>{{myboolean}}</span>
  <h2 :class="{bordered:myboolean}">bordered on condition</h2>
  <h2 v-if="myboolean">reveal on myboolean</h2>
</template>
<script>
export default {
  data(){ // data itself starts
    return{ // data variables starts
      myboolean : false
    } // data variables end
  }, // data itself ends
  methods:{ // methods (functions) start
    // we write functions in here
    // if we write multiple functions we separate them with comma ,
    mybool_reverse(){
      // in framework environment 'this.' refers to 'this variable is from this component.vue data area'
      // so in almost all cases when we use a data variable we need to put this. infront of it 
      this.myboolean = !this.myboolean;
    }
  } // methods (functions) end
}
</script>
<style>
h1{
  background-color: antiquewhite;
  padding: 10px;
  border-radius: 10px;
  border: 1px solid black;
}
.bordered{border: 1px solid black;}
</style>