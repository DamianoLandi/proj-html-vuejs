<template>
    <div>
        <!-- Footer Links -->
        <section id="links">
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

        <!-- Copyright & Social Media -->
        <section id="bottom-footer">
            <div class="container row bf-row">
                <p class="text-gray"> &#169; Copyright 2012 - 2020 | Avada Theme by <span>Theme Fusion</span> | All Rights Reserved | Powered by <span>WordPress</span></p>
                <div class="icons-container">
                    <div class="bg-darkblue icon-bg">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                    </div>
                    <div class="bg-lightblue icon-bg">
                        <a href="#"><i class="fab fa-twitter"></i></a>
                    </div>
                    <div class="bg-blue icon-bg">
                        <a href="#"><i class="fab fa-instagram"></i></a>
                    </div>
                    <div class="bg-red icon-bg">
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
            </div>
            <div id="to-top">
                <a href="#"><i class="fas fa-chevron-up"></i></a>
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

<style scoped lang="scss">

/* Links */

#links{
    padding: 50px 0;
    border-bottom: 2px solid lightgray;
}

.row{
    display: flex;
}

.col-3{
    flex-basis: calc(100% / 4);
    padding: 20px;
    margin-top: 75px;
}

/* Bottom Footer */

#bottom-footer{
    position: relative;
}

p{
    font-size: 13px;
    span{
        color: #000;
    }
}


.bf-row{
    justify-content: space-between;
    align-items: center;
    height: 100px;
    .icons-container{
        flex-basis: 20%;
        display: flex;
        justify-content: space-between;
        .icon-bg{
            height: 50px;
            width: 50px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            a{
                font-size: 20px;
                color: white;
                text-decoration: none;
            }
        }
    }
}

/* To-Top Button */

#to-top{
    position: absolute;
    bottom: 0;
    right: 100px;
    height: 35px;
    width: 35px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #62676c;
    border-radius: 3px 3px 0 0;
    a{
        color: white;
    }
}

/* Icons BG-Color */

.bg-darkblue{
    background-color: #4562b0;
}

.bg-blue{
    background-color: #516faa;
}

.bg-lightblue{
    background-color: #74def4;
}

.bg-red{
    background-color: #951a0c;
}

</style>