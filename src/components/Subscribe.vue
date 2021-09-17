<template>
    <div class="container-subscribe">
        <h2>Subscribe to our Newsletter</h2>
        <div class="input-container">
            <input type="email" name="subscribe" id="subscribe" placeholder="Insert your email*">
            <button>Send</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "Subscribe,"
}
</script>

<style scoped>
    .container-subscribe{
        height: 100%;
        background-color: #F2F2F2;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .input-container{
        width: 550px;
        display: flex;
        justify-content: space-between;
    }

    input{
        padding: 10px 180px 10px 10px;
        border: 1px solid lightgray;
    }

    button{
        color: white;
        text-transform: uppercase;
        background-color: #25A9BD;
        padding: 10px 60px;
        border-color: transparent;
        font-weight: 600;
    }
</style>