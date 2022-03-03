<template>
    <main>
        <div class="container">
            <mainJournal />
        </div>
    </main>
</template>

<script>
    import mainJournal from "./main/mainJournal.vue"

    export default {
        name:"myMain",
        components:{
            mainJournal
        }
    }
</script>

<style scoped lang="scss">
    @import "./SCSS/colors.scss";

    main{
        background-color: $mainBackground;
        height: 100vh;

        
        
    }
</style>