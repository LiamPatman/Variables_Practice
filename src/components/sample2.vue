<template>
  <!-- all HTML content -->
  <!-- other components also are used in template area-->
  <!-- we can add a CSS class on a CONDITION based on a boolean variable -->
  <!-- below example CSS class 'disabled' applies to element ONLY when variable 'disabled_condition' is TRUE -->
  <div class="information" :class="{disabled : disabled_condition}">
    <h3>some info</h3>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illum assumenda nobis fugiat autem, ullam temporibus ex architecto dignissimos non quasi?</p>
  </div>

</template>
<style scoped>
  /* all CSS classes are defined here */
  .information{
    background-color: blueviolet;
    color: white;
    padding: 10px;
    border-radius: 10px;
  }
  .disabled{
    background-color: gray !important;
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
      disabled_condition : true
    } // data End
  }
}
</script>