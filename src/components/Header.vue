<template>
    <header>

        <!-- Logo & Navbar -->
        <div class="container">
            <img src="../assets/img/logo.png" alt="Logo" id="logo">
            <ul>
                <li v-for="(link, index) in headerLinks" :key="index"><a :href="link.url">{{link.text}}</a><div class="active"></div></li>
                <li><button>Join us</button></li>
                <li><i class="fas fa-search"></i></li>
            </ul>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",
    data(){
        return{
            headerLinks: [
                {
                    text: "Home",
                    url: "#",
                },
                {
                    text: "Apple",
                    url: "#",
                },
                {
                    text: "Microsoft",
                    url: "#",
                },
                                {
                    text: "Android",
                    url: "#",
                },
                {
                    text: "Forums",
                    url: "#",
                },
                {
                    text: "Contact us",
                    url: "#",
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">

    /* Style */

    header{
        height: 80px;
        background-color: #4A4A4A;
        .container{
            height: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            ul{
                flex-basis: 50%;
                display: flex;
                justify-content: space-between;
                align-items: center;
                li{
                    position: relative;
                    color: white;
                    a{
                        color: white;
                        text-decoration: none;
                    }
                    button{
                        color: white;
                        background-color: #202325;
                        border-color: transparent;
                        text-transform: uppercase;
                        padding: 7px 15px;
                        cursor: pointer;
                    }

                }
            }
        }
    }

    /* Hover Effect */

    .active{
        height: 20px;
        width: 20px;
        background-color: #4A4A4A;
        position: absolute;
        transform: rotate(45deg);
        left: 35%;
        top: 35px;
        display: none;
    }

    li:hover .active{
        display: inline-block;
    }
</style>