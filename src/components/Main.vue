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
                    <ul>
                        <li v-for="(item, index) in sideNews" :key="index">
                            <CardSmall :item="item"/>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="section-footer">
                <a href="#">Read our blog &rarr;</a>
            </div>
        </section>
        <section id="forums">
            <div class="section-header">
                <h3>Phasellus eget metus</h3>
                <h2>Forum Sections</h2>
                <hr>
            </div>
            <div class="container cards-container">
                <div class="col-3" v-for="(item, index) in forumSections" :key="index">
                    <ForumCard :item="item"/>
                </div>
            </div>
            <div class="section-footer">
                <a href="#">Go to our forum &rarr;</a>
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
import CardSmall from "./CardSmall.vue"
import ForumCard from "./ForumCard.vue"

export default {
    name: "Footer",
    components:{
        Jumbo,
        MainText,
        NewsCard,
        Featured,
        FeaturedSmall,
        CardSmall,
        ForumCard
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
            ],
            sideNews:[
                {
                    imgUrl: "post_feat_img_23-320x202.jpg",
                    title: "Morbi vitae dui euismod vulputate sullicitund",
                    date: "October 11th, 2015",
                    comments: 2,
                },
                {
                    imgUrl: "post_feat_img_22-320x202.jpg",
                    title: "Morbi vitae dui euismod vulputate sullicitund",
                    date: "October 11th, 2015",
                    comments: 0,
                },
                {
                    imgUrl: "post_feat_img_20-320x202.jpg",
                    title: "Morbi vitae dui euismod vulputate sullicitund",
                    date: "October 11th, 2015",
                    comments: 0,
                }
            ],
            forumSections: [
                {
                    icon: "fas fa-file-alt",
                    text: "News & Community"
                },
                {
                    icon: "fab fa-apple",
                    text: "Apple Forum"
                },
                {
                    icon: "fab fa-windows",
                    text: "Microsoft Forum"
                },
                {
                    icon: "fab fa-android",
                    text: "Android Forum"
                },
                {
                    icon: "fas fa-coffee",
                    text: "General Discussion"
                },
                {
                    icon: "fas fa-cubes",
                    text: "Apps & Software"
                },
                {
                    icon: "fas fa-laptop",
                    text: "Gadgets & Stuff"
                },
                {
                    icon: "fas fa-wrench",
                    text: "Tutorials & Guides"
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
    flex-wrap: wrap;
    justify-content: space-between;
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

.col-3{
    flex-basis: calc(100% / 4);
}

ul{
    list-style-type: none;
    padding: 0;
}

.section-footer{
    background-color: #25A9BD;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100px;
    margin-top: 30px;
}

.section-footer a{
    color: white;
    text-decoration: none;
    font-size: 15px;
    text-transform: uppercase;
    font-weight: 600;
}

#forums{
    margin-top: 0;
    padding-top: 100px;
    background-color: #F2F2F2;
}

</style>