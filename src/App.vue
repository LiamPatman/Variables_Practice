<template>
  <LandingVue />

  <section class="results-section">
    <VehicleVue v-for='vehicle in vehicles_array'  :vehicle_obj='vehicle' />
  </section>

</template>

<style scoped>

</style>

<script setup>
  import VehicleVue from './components/15th Feb_e2(arrays)_content.vue'
</script>

<script>
export default {
  data(){
    return{
      vehicles_array : [
        {
          type : 'Motorbike',
          min_people : 1,
          max_people : 1,
          min_day : 1,
          max_day : 5,
          price_per_day : 109,
          gas_per_100km : 3.7
        },
        {
          type : 'Small Car',
          min_people : 1,
          max_people : 2,
          min_day : 1,
          max_day : 5,
          price_per_day : 129,
          gas_per_100km : 8.5
        }
      ]
    }
  }
}
</script>