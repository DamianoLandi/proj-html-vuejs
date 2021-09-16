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
                </div>
            </div>
            <div class="container">
                <Featured/>
            </div>
            <div class="container cards-container">
                <div class="col" v-for="(item, index) in secondNews" :key="index">
                    <NewsCard :item="item"/>
                </div>
            </div>
            <div class="container row">
                <div class="col-8">
                    <FeaturedSmall/>
                </div>
                <div class="col-4">
                    <h2 id="sidebar-header">Tutorials & Guides</h2>
                    <hr id="sidebar-divider">
                </div>
            </div>
        </section>
    </main>
</template>

<script>
import Jumbo from "./Jumbo.vue"
import MainText from "./MainText.vue"
import NewsCard from "./NewsCard.vue"
import Featured from "./Featured.vue"
import FeaturedSmall from "./FeaturedSmall.vue"

export default {
    name: "Footer",
    components:{
        Jumbo,
        MainText,
        NewsCard,
        Featured,
        FeaturedSmall,
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
            ],
            secondNews:[
                {
                    imgUrl: "post_feat_img_22-320x202.jpg",
                    title: "Morbi vitae dui euismod vulputate sullicitund",
                    date: "October 11th, 2015",
                    comments: 0,
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Error, illo beatae? Voluptates, atque dolorem ut enim beatae vero esse animi impedit, voluptas dignissimos provident iusto libero necessitatibus nihil fuga at!"
                },
                {
                    imgUrl: "post_feat_img_21-320x202.jpg",
                    title: "Morbi vitae dui euismod vulputate sullicitund",
                    date: "October 11th, 2015",
                    comments: 0,
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Error, illo beatae? Voluptates, atque dolorem ut enim beatae vero esse animi impedit, voluptas dignissimos provident iusto libero necessitatibus nihil fuga at!"
                },
                {
                    imgUrl: "post_feat_img_20-320x202.jpg",
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

<style scoped>
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

#sidebar-header{
    margin-top: 0;
}

#sidebar-divider{
    margin: 0
}

.cards-container{
    display: flex;
}

.col{
    flex-basis: 33%;
}

.row{
    display: flex;
    justify-content: space-between;
}

.col-8{
    flex-basis: calc(100% / 3 * 2);
    padding: 10px;
}

.col-4{
    flex-basis: calc(100% / 3);
    padding: 0 30px;
}

</style>