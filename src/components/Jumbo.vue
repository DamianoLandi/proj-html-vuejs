<template>
    <div class="jumbo">
        <div class="container">
            <h1>Tech Forum!</h1>
            <p>Discuss all the latest technology news and trends</p>
            <a href="#">Get Avada Now! <i class="fas fa-chevron-right"></i></a>
        </div>
    </div>
</template>

<script>
export default {
    name: "Jumbo",
}
</script>

<style scoped lang="scss">
    .jumbo{
        height: 870px;
        background-image: url("../assets/img/home_slider_bg.jpg");
        .container{
            display: flex;
            flex-direction: column;
            justify-content: center;
            height: 100%;
            color: white;
            h1{
                font-size: 135px;
                margin: 0;
            }

            p{
                font-size: 20px;
            }
    
            a{
                color: white;
                text-decoration: none;
                display: inline-block;
                background-color: #4A4A4A;
                width: 150px;
                text-align: center;
                padding: 10px 20px;
                text-transform: uppercase;
                font-size: 13px;
                font-weight: 600;
            }
        }
    }

</style>