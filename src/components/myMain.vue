<template>
    <main>
        <div class="container">
            <mainJournal />

            <mainRecipes :listaImmagini="recipesImages"/>

            <mainCookCollection :imagesList="culinaryImages"/>

            <mainSocialBlog :cardsList="socialBlogCards"/>

        </div>

        <!--il componente newsletter fuori dal container, dato che dovrà occupare l'intera larghezza-->
        <mainNewsletter />


    </main>
</template>

<script>
    import mainJournal from "./main/mainJournal.vue"
    import mainRecipes from "./main/mainRecipes.vue"
    import mainCookCollection from "./main/mainCookCollection.vue"
    import mainSocialBlog from "./main/mainSocialBlog.vue"
    import mainNewsletter from "./main/mainNewsletter.vue"




    export default {
        name:"myMain",
        components:{
            mainJournal,
            mainRecipes,
            mainCookCollection,
            mainSocialBlog,
            mainNewsletter
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
                ],

                //lista carte del componente socialBlog
                socialBlogCards: [
                    {
                        url: "fi-roundup-400x263.jpg",
                        title: "Roundup: My New Favourite Recipes for Healty Living",
                        author: "By Admin, March 25th 2019"
                    },
                    {
                        url: "fi-korean-food-400x263.jpg",
                        title: "Metal Prep: Krean bibimbap with kimchi",
                        author: "By Admin, March 25th 2019"
                    },
                    {
                        url: "fi-toasts-400x263.jpg",
                        title: "Why These Toasts with Tea are My new Favourite",
                        author: "By Admin, March 25th 2019"
                    },
                    {
                        url: "fi-street-food-400x263.jpg",
                        title: "Exploring street food in Bangkok",
                        author: "By Admin, March 25th 2019"
                    },
                    {
                        url: "fi-organic-breakfast-400x263.jpg",
                        title: "Organic choices for Healthier living",
                        author: "By Admin, March 25th 2019"
                    },
                    {
                        url: "fi-water-side-rest-400x263.jpg",
                        title: "5 waterside restaurants in Instanbul for special events",
                        author: "By Admin, March 25th 2019"
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