<template>
    <div class="register-bg"> 
        <div class="container-xs">
            <h2>Hey! Join to our Community!</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti debitis cupiditate enim iure adipisci architecto sunt.</p>
            <a href="#">Sign up <i class="fas fa-chevron-right"></i></a>
        </div>
    </div>
</template>

<script>
export default {
    name: "Register"
}
</script>

<style scoped lang="scss">
    .register-bg{
        height: 100%;
        background-image: url("../assets/img/join_now_cta_bg.jpg");
        background-size: cover;
        background-position: center;
        color: white;
        .container-xs{
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            h2{
                font-size: 45px;
            }

            a{
                color: white;
                background-color: #202325;
                border: 1px solid #202325;
                text-transform: uppercase;
                padding: 10px 20px;
                cursor: pointer;
                text-decoration: none;
            }
        }
    }

</style>