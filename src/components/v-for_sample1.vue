<template>
  <!-- all HTML content -->
  <!-- other components also are used in template area-->
  <!-- v-for creates multiple duplicates of the element (incluuding all its content) as many times as there are items in the array given -->
  <!-- structure is v-for='variableName in arrayName' -->
  <!-- variableName then becomes each one of the items in the array (the value itself, not index position) -->
  <h1 v-for="title in titles_array">{{ title }}</h1>
</template>
<style scoped>
  /* all CSS classes are defined here */
</style>
<script setup>
  // all imports for other components are done in setup
  // Prop declarations also are done in script setup
</script>
<script>
export default {
  data(){
    return{ // data Start
      titles_array:[
        'title one',
        'title two',
        'title three',
        'title four'
      ]
    } // data End
  }
}
</script>