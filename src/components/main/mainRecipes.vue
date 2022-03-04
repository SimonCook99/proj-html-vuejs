<template>
    <section class="popular-recipes">


        <!--mainIntroduction è la parte introduttiva della sezione, a cui passo le scritte come props-->
        <mainIntroduction 
            title="popular recipes"
            description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius ea deserunt, iure nesciunt rem ratione dignissimos sunt"
        />

        <!--riga principale della sezione-->
        <div class="row main-row">

            <!--contenitore della ricetta principale-->
            <div class="main-recipe col-6">
                <img src="../../assets/img/Yogurt-Nan-600x395.jpg" alt="Yogurt nan">
                
                <div class="info">
                    <h4>Lunch favourite with salad, Naan and beans</h4>
                    <p>Bakery, featured, healthy, Latest recipes, Staff picks</p>

                    <hr>

                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis, nulla eum. Culpa tempora expedita cumque dolorem ad corrupti eligendi quas, ullam porro? Doloribus, consequatur eos molestias eveniet velit accusamus nostrum?</p>
                    <button>Learn more</button>
                </div>

            </div>

            <!--contenitore delle altre ricette secondarie-->
            <div class="other-recipes col-6">
                <div class="row">
                    <div class="col-6" v-for="(image, index) in listaImmagini" :key="index">
                        
                        
                        <img :src="require('../../assets/img/' + image.url)"  :alt="image.alt">
                    </div>
                    
                </div>
                
            </div>
        </div>
    </section>
</template>

<script>

    import mainIntroduction from "./partials/mainIntroduction.vue";

    export default {
        name: "mainRecipes",
        components:{
            mainIntroduction
        },
        
        props: {
            "listaImmagini": Array
        }
    }
</script>

<style scoped lang="scss">

    @import "../SCSS/colors.scss";

    img{
        width: 100%;
    }

    .main-row{
        flex-wrap: nowrap;
    }

    

    .main-recipe{
        background-color: white;
        padding: 0;
        margin-right: 20px;

        img{
            width: 100%;
        }
    }

    .info{
        padding: 30px;

        h4{
            margin-top: 10px;
        }

        hr{
            margin: 20px 0px;
        }

        button{
            padding: 10px 20px;
        }
    }

    .other-recipes{
        .col-6{
            margin-bottom: 20px;
        }
    }
    
</style>