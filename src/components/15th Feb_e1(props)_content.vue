<template>
 <h1>{{ Heading_Msg }}</h1>
</template>
<style scoped>
  /* all CSS classes are defined here */
  h1{background-color: antiquewhite;}
</style>
<script setup>
// when a component is meant to receive data from its parent component
// we declare a prop system with the code below
defineProps({
  Heading_Msg: { //'Heading_Msg' is the variable name we to it in this example, and you can name it however you want
    type: String, // String, Number, Array, Object, Boolean
    required: true
  }
});
</script>