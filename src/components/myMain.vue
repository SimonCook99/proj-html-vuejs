<template>
    <main>
        <div class="container">
            <mainJournal />

            <mainRecipes :listaImmagini="recipesImages"/>

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
        },
        data(){
            return{
                recipesImages:[
                    {
                        url: "Mixed-fruits-400x263.jpg",
                        alt: "frutta mista"
                    },
                    {
                        url: "r-rachel-park-366508-unsplash-min-400x263.jpg",
                        alt: "rachel park"
                    },
                    {
                        url: "r-michelle-tsang-500721-unsplash-min-400x263.jpg",
                        alt: "ice cream"
                    },
                    {
                        url: "quick-summer-drink-460x295.jpg",
                        alt: "summer drink"
                    },
                    {
                        url: "r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg",
                        alt: "vegetables"
                    },
                    {
                        url: "perfect-cosmopolitan-460x295.jpg",
                        alt: "cosmopolitan"
                    },
                    {
                        url: "fi2x-6-460x295.jpg",
                        alt: "menu"
                    },
                    {
                        url: "r-brooke-lark-96398-unsplash-min-460x295.jpg",
                        alt: "cakes"
                    },
                    
                ]
            }
        }
    }
</script>

<style scoped lang="scss">
    @import "./SCSS/colors.scss";

    main{
        background-color: $mainBackground;

    }
</style>