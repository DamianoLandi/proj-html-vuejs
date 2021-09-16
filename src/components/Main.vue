<template>
    <main>
        <section id="jumbo">
            <Jumbo/>
            <MainText/>
        </section>
        <section id="news">
            <div class="section-header">
                <h3>Phasellus eget metus</h3>
                <h2>All the latest news</h2>
                <hr>
            </div>
            <div class="container cards-container">
                <div class="col" v-for="(item, index) in firstNews" :key="index">
                    <NewsCard :item="item"/>
                    <img src="" alt="">
                </div>
            </div>
        </section>
    </main>
</template>

<script>
import Jumbo from "./Jumbo.vue"
import MainText from "./MainText.vue"
import NewsCard from "./NewsCard.vue"

export default {
    name: "Footer",
    components:{
        Jumbo,
        MainText,
        NewsCard
    },
    data(){
        return{
            firstNews:[
                {
                    imgUrl: "post_feat_img_25-320x202.jpg",
                    title: "Morbi vitae dui euismod vulputate sullicitund",
                    date: "October 11th, 2015",
                    comments: 2,
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Error, illo beatae? Voluptates, atque dolorem ut enim beatae vero esse animi impedit, voluptas dignissimos provident iusto libero necessitatibus nihil fuga at!"
                },
                {
                    imgUrl: "post_feat_img_24-320x202.jpg",
                    title: "Morbi vitae dui euismod vulputate sullicitund",
                    date: "October 11th, 2015",
                    comments: 0,
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Error, illo beatae? Voluptates, atque dolorem ut enim beatae vero esse animi impedit, voluptas dignissimos provident iusto libero necessitatibus nihil fuga at!"
                },
                {
                    imgUrl: "post_feat_img_23-320x202.jpg",
                    title: "Morbi vitae dui euismod vulputate sullicitund",
                    date: "October 11th, 2015",
                    comments: 0,
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Error, illo beatae? Voluptates, atque dolorem ut enim beatae vero esse animi impedit, voluptas dignissimos provident iusto libero necessitatibus nihil fuga at!"
                }
            ]
        }
    }
}
</script>

<style>
#news{
    margin-top: 100px;
}

.section-header{
    text-align: center;
    color: #202325;
}

.section-header h3{
    font-size: 20px;
    text-transform: uppercase;
}

.section-header h2{
    font-size: 45px;
}

hr{
    border-color: #fc8c5e;
    width: 100px;
}

.cards-container{
    display: flex;
}

.col{
    flex-basis: 33%;
}

</style>