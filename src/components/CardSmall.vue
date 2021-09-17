<template>
    <!-- Template delle cards per gli articoli in evidenza -->

    <div class="card">
        <img :src="require('@/assets/img/' + item.imgUrl)" alt="img">
        <div>
            <h3>{{item.title}}</h3>
            <p><span class="text-gray">{{item.date}}</span> | <span v-if="item.comments != 0">{{item.comments}} Comments</span> <span class="text-gray" v-else>No Comments</span></p>
        </div>
    </div>
</template>

<script>
export default {
    name: "CardSmall",
    props: [
        "item",
    ]
}
</script>

<style scoped lang="scss">
    .card{
        display: flex;
        max-height: 165px;
        img{
            width: 200px;
            padding-right: 20px;
            padding-bottom: 20px;
        }
        h3{
            font-size: 14px;
        }
    }
</style>