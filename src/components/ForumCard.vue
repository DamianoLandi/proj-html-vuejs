<template>
    <!-- Template delle cards per le Forum Sections-->
    <div class="card">
        <div class="icon-bg">
            <i :class="item.icon"></i>
        </div>
        <h3>{{item.text}}</h3>
    </div>
</template>

<script>
export default {
    name: "ForumCard",
    props: [
        "item"
    ]
}
</script>

<style scoped lang="scss">
    .card{
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        height: 200px;
        margin: 50px auto;
        border-top: 5px solid #4A4A4A;
        width: 75%;
        padding: 25px 0;
        cursor: pointer;
        background-color: #fff;
        .icon-bg{
            height: 100px;
            width: 100px;
            border-radius: 50%;
            background-color: #fc8c5e;
            display: flex;
            justify-content: center;
            align-items: center;
            i{
                font-size: 35px;
                color: white;
            }
        }
    }
</style>