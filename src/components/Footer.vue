<template>
    <div>
        <section class="links">
            <div class="container row">
                <div class="col-3">
                    <h2>Avada Tech Forum</h2>
                    <p class="text-gray">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aspernatur dolorem voluptatum repellat praesentium odit amet maxime mollitia! Possimus molestiae ex iste est odio cumque, saepe maiores itaque eos, impedit aliquam.</p>
                </div>
                <div class="col-3" v-for="(list, index) in lists" :key="index">
                    <FooterList :list="list"/>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import FooterList from "./FooterList.vue"

export default {
    name: "Footer",
    components: {
        FooterList,
    },
    data(){
        return{
            lists:[
                {
                    listHeader: "Popular Topics",
                    links:[
                        "Aspernatur dolorem voluptatum repellat",
                        "Aspernatur dolorem voluptatum repellat",
                        "Aspernatur dolorem voluptatum repellat",
                        "Aspernatur dolorem voluptatum",
                    ]
                },
                {
                    listHeader: "Recent Topics",
                    links: [
                        "Lorem ipsum, dolor sit amet consectetur adipisicing elit",
                        "Lorem ipsum, dolor sit amet consectetur adipisicing elit",
                        "Lorem ipsum, dolor sit amet consectetur adipisicing elit",
                        "Lorem ipsum, dolor sit amet consectetur adipisicing elit",
                    ]
                },
                {
                    listHeader: "Latest Replies",
                    links: [
                        "Possimus molestiae ex iste est odio cumque, saepe maiores",
                        "Possimus molestiae ex iste est odio cumque, saepe maiores",
                        "Possimus molestiae ex iste est odio cumque, saepe maiores",
                        "Possimus molestiae ex iste est odio cumque, saepe maiores",
                    ]
                }
            ]
        }
    }
}
</script>

<style scoped>

.row{
    display: flex;
}

.col-3{
    flex-basis: calc(100% / 4);
    padding: 20px;
    margin-top: 75px;
}

.text-gray{
    color: #62676c;
}
</style>