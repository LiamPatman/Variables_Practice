<template>
    <div class="content-div" :class="{approvedCSS:content_obj.approved}">
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
defineProps({
  content_obj: {
    type: Object,
    required: true
  }
});
</script>