<template>
    <div class="card">
        <img :src="require('@/assets/img/' + item.imgUrl)" alt="img">
        <h3>{{item.title}}</h3>
        <p><span>{{item.date}}</span> | <span v-if="item.comments != 0">{{item.comments}} Comments</span> <span v-else>No Comments</span></p>
        <p>{{item.text}}</p>
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

<style>

</style>