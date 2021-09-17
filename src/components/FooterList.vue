<template>
    <div>
        <h2>{{list.listHeader}}</h2>
        <ul>
            <li v-for="(link, index) in list.links" :key="index"><a href="#"><i class="fas fa-chevron-right"></i> {{link}}</a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "FooterList",
    props:[
        "list"
    ]
}
</script>

<style scoped>

    ul{
        padding: 0;
        list-style-type: none;
    }

    li{
        border-bottom: 1px solid lightgray;
        line-height: 35px;
        margin-left: 7px;
        text-indent: -7px;
    }

    a{
        color: black;
        text-decoration: none;
    }

    i{
        font-size: 10px;
    }
</style>