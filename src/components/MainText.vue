<template>
    <div>
        <div class="container-small"> 
            <h2>Avada Forum is the place to be</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta fugiat dignissimos culpa harum labore nam alias neque libero, quas voluptatum. Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
        </div>
    </div>
</template>

<script>
export default {
    name: "MainText"
}   
</script>

<style scoped>
    div{
        background-color: #F2F2F2;
        text-align: center;
        height: 500px;
    }

    .container-small{
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    h2{
        margin: 0;
        color: #202325;
        text-transform: uppercase;
        font-weight: 600;
        font-size: 18px;
    }

    p{
        color: #62676c;
        line-height: 40px;
        font-size: 24px;
    }

</style>