<template>
    <div class="vehicle-div">
        <h2>{{ vehicle_obj.type }}</h2>
        <p>Range of people is {{vehicle_obj.min_people}} to {{vehicle_obj.max_people}}</p>
        <p>Range of days is {{vehicle_obj.min_day}} to {{vehicle_obj.max_day}}</p>
        <p>Costs ${{vehicle_obj.price_per_day}} per day</p>
        <p>Uses {{vehicle_obj.gas_per_100km}}L of gas per 100km</p>
    </div>
</template>

<style scoped>
.vehicle-div{
    flex: 1;
    background-color: purple;
    color: aliceblue;
    border-radius: 10px;
    padding: 10px;
}
</style>

<script setup>

defineProps({
    vehicle_obj: {
        type: Object,
        required: true
    }
})
</script>