<template>
    <main>
        <div class="container">
            <mainJournal />

            <mainRecipes :listaImmagini="recipesImages"/>

            <mainCookCollection :imagesList="culinaryImages"/>

        </div>
    </main>
</template>

<script>
    import mainJournal from "./main/mainJournal.vue"
    import mainRecipes from "./main/mainRecipes.vue"
    import mainCookCollection from "./main/mainCookCollection.vue"


    export default {
        name:"myMain",
        components:{
            mainJournal,
            mainRecipes,
            mainCookCollection
        },
        data(){
            return{

                //lista immagini della sezione recipes
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
                ],

                //lista immagini della sezione culinary collection
                culinaryImages:[
                    {
                        url: "drinks-recipes.png",
                        type: "drinks"
                    },
                    {
                        url: "soups-recipes.png",
                        type: "soups"
                    },
                    {
                        url: "baking-recipes.png",
                        type: "bakery"
                    },
                    {
                        url: "dinner-recipes.png",
                        type: "dinner"
                    },
                    {
                        url: "healthy-recipes.png",
                        type: "healthy"
                    },
                    {
                        url: "staff-picks.png",
                        type: "staff picks"
                    },
                    {
                        url: "premium-recipes.png",
                        type: "appetisers"
                    },
                    {
                        url: "quick-easy-recipes.png",
                        type: "quick & easy"
                    }
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