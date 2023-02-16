<script setup>
  import PersonVue from './components/Person.vue'
</script>

<template>
  <PersonVue v-for='person_item in my_data_array'
  :person_obj='person_item' />
</template>

<script>
export default {
  data(){ 
    return{
      my_data_array:[
        {
          fname : 'Utku',
          lname : 'Yalcin',
          present : false
        },
        {
          fname : 'Tin',
          lname : 'Baltazar',
          present : false
        },
        {
          fname : 'Katie',
          lname : 'Pragg',
          present : false
        },
        {
          fname : 'Merlin',
          lname : 'Stemmer',
          present : false
        },
      ]
    }
  }
}
</script>

<style>

</style>