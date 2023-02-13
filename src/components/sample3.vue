<template>
  <!-- all HTML content -->
  <!-- other components also are used in template area-->
  <!-- we can add a CSS class on a CONDITION based on a boolean variable -->
  <!-- below example CSS class 'disabled' applies to element ONLY when variable 'disabled_condition' is TRUE -->
  <!-- multiple CSSclass : Boolean pairings can be put in { } you just need to separate with comma , -->
  <!-- e.g. :class="{CSS-class-one : BooleanA , CSS-class-two : BooleanB}" -->
  <div class="information" :class="{disabled : disabled_condition}">
    <h3>some info</h3>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illum assumenda nobis fugiat autem, ullam temporibus ex architecto dignissimos non quasi?</p>
  </div>

  <!-- if we want to use more than one v-binded: css classes we place them inside [ ] and separate them with comma , (almost like an array) -->
  <span :class="[myColor, myBGColor]">colored</span>
  <span class="green orangeBG">colored</span>
  <!-- we can also combine v-binded: CSS classes AND conditional binded css classes together in [ ] -->
  <span :class="[myColor, {disabled:disabled_condition}]">disabled colored</span>
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
  .green{color: green;}
  .blue{color: blue;}
  .orangeBG{background-color: orange;}
</style>
<script setup>
  // all imports for other components are done in setup
  // Prop declarations also are done in script setup
</script>
<script>
export default {
  data(){
    return{ // data Start
      disabled_condition : true,
      myColor : 'green',
      myBGColor : 'orangeBG'
    } // data End
  }
}
</script>