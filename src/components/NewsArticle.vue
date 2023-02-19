<template>
    <div class="news-article">



    </div>
</template>

<style scoped>
.news-article{

}
.news-thumb{

}
.content{
    
}
</style>

<script setup>
defineProps({
    NewsArticleObj: {
        type: Object,
        required: true
    }
});
</script>

<script>
export default {
    data() {
        return{
            content_reveal : false
        }
    },
}
</script>