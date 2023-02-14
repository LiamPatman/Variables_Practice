// This content links with 'contentForLoop' file
// This content goes into App file

<template>
  <!-- all HTML content -->
  <!-- other components also are used in template area-->
  <ContentVue v-for="content in contents_array" :content_obj="content" />
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
      contents_array:[
        {
          title:'title one',
          content:'content one',
          content_revealed:true,
          approved:true
        },
        {
          title:'title two',
          content:'content two',
          content_revealed:true,
          approved:false
        },
        {
          title:'title three',
          content:'content three',
          content_revealed:false,
          approved:true
        }
      ]
    } // data End
  }
}
</script>