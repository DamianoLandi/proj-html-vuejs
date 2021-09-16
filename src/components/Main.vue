<template>
    <main>
        <section>
            <Jumbo/>
            <MainText/>
        </section>
    </main>
</template>

<script>
import Jumbo from "./Jumbo.vue"
import MainText from "./MainText.vue"

export default {
    name: "Footer",
    components:{
        Jumbo,
        MainText,
    }
}
</script>

<style>

</style>