<template>
  <!-- all HTML content -->
  <!-- other components also are used in template area-->
  <!-- v-for creates multiple duplicates of the element (incluuding all its content) as many times as there are items in the array given -->
  <!-- structure is v-for='variableName in arrayName' -->
  <!-- variableName then becomes each one of the items in the array (the value itself, not index position) -->
  
  <div class="content-div" v-for="content_obj in contents_array" :class="{approvedCSS:content_obj.approved}">
    <h2>{{ content_obj.title }}</h2>
    <p v-if="content_obj.content_revealed">{{ content_obj.content }}</p>
  </div>

</template>
<style scoped>
  /* all CSS classes are defined here */
  .content-div{
    border: 1px solid black;
    padding: 10px;
    margin: 5px;
  }
  .approvedCSS{background-color: limegreen;}
</style>
<script setup>
  // all imports for other components are done in setup
  // Prop declarations also are done in script setup
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