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
    header{
        height: 80px;
        background-color: #4A4A4A;
    }

    .container{
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    ul{
        flex-basis: 50%;
        list-style-type: none;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    li{
        position: relative;
    }

    li, li a{
        color: white;
    }

    li a{
        text-decoration: none;
    }

    button{
        color: white;
        background-color: #202325;
        border: 1px solid #202325;
        text-transform: uppercase;
        padding: 7px 15px;
        cursor: pointer;
    }

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