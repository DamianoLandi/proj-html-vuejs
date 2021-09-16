<template>
    <div class="card">
        <img :src="require('@/assets/img/' + item.imgUrl)" alt="img">
        <h3>{{item.title}}</h3>
        <p><span class="text-gray">{{item.date}}</span> | <span v-if="item.comments != 0">{{item.comments}} Comments</span> <span class="text-gray" v-else>No Comments</span></p>
        <p class="text-gray">{{item.text}}</p>
    </div>
</template>

<script>

export default {
    name: "NewsCard",
    props: [
        "item",
    ]
}
</script>

<style scoped>
    .card{
        padding: 15px;
    }

    img{
        width: 100%;
    }

    .text-gray{
        color: #62676c;
    }
</style>