<template>
    <div class="person-div" :class="{presentCSS:person_obj.present}"
    @click="person_obj.present = !person_obj.present">

        <h3>{{person_obj.fname}} {{person_obj.lname}}</h3>
    </div>
</template>

<style scoped>
.person-div{
    border: 2px solid gray;
    border-radius: 10px;
    background-color: lightgray;
    padding: 10px;
    margin: 5px;
}
.presentCSS{
    border: 2px solid blue;
    background-color: lightblue;
}
</style>

<script setup>
    defineProps({
        person_obj: {
            type: Object,
            required: true
        }
    });
</script>