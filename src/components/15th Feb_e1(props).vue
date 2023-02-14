<template>
  <!-- all HTML content -->
  <!-- other components also are used in template area-->
  <ContentVue Heading_Msg='My Message' /> <!-- we need to use EXACT same Prop name that's declared in the component with prop -->
  <ContentVue :Heading_Msg='myVariable'/>
  <ContentVue :Heading_Msg='otherVariable' />
</template>
<style scoped>
  /* all CSS classes are defined here */
</style>
<script setup>
  // all imports for other components are done in setup
  // Prop declarations also are done in script setup
  import ContentVue from './components/Content.vue'
</script>
<script>
export default {
  data(){
    return{ // data Start
      myVariable : 'hello world',
      otherVariable : 'test message'
    } // data End
  }
}
</script>