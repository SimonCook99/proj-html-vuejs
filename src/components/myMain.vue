<template>
    <main>
        <div class="container">
            <mainJournal />

            <mainRecipes />

        </div>
    </main>
</template>

<script>
    import mainJournal from "./main/mainJournal.vue"
    import mainRecipes from "./main/mainRecipes.vue"


    export default {
        name:"myMain",
        components:{
            mainJournal,
            mainRecipes
        }
    }
</script>

<style scoped lang="scss">
    @import "./SCSS/colors.scss";

    main{
        background-color: $mainBackground;

    }
</style>