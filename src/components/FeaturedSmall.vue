<template>
    <div class="featured-small">
        <h3>Reviewed Product</h3>
        <h2>Lorem ipsum dolor sit amet consectetur.</h2>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Cum, sequi distinctio explicabo pariatur blanditiis nobis eos doloribus natus animi provident eveniet dolores tenetur temporibus, non voluptatem modi ratione deserunt porro?</p>
        <a href="#">Read More <i class="fas fa-chevron-right"></i></a>
    </div>
</template>

<script>
export default {
    name:"FeaturedSmall"
}
</script>

<style scoped>
    .featured-small{
        background-image: url("../assets/img/featured_article_2_bg.jpg");
        height: 550px;
        background-position: center;
        background-size: cover;
        color: white;
        margin-bottom: 50px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 0 50px;
    }

    h3{
        text-transform: uppercase;
        font-size: 15px;
    }

    h2{
        font-size: 35px;
    }

    a{
        color: white;
        text-decoration: none;
        display: inline-block;
        background-color: #25A9BD;
        width: 150px;
        text-align: center;
        padding: 10px 20px;
        text-transform: uppercase;
        font-size: 13px;
        font-weight: 600;
    }
</style>