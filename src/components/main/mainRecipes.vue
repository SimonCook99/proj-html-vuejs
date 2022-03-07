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

                <div class="overlay">
                    <i class="fa-solid fa-link"></i>
                    <h5>Lunch favourite with salad, Naan and beans</h5>
                </div>
                
                <div class="info">
                    <h4>Lunch favourite with salad, Naan and beans</h4>
                    <p>Bakery, featured, healthy, Latest recipes, Staff picks</p>

                    <hr>

                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis, nulla eum. Culpa tempora expedita cumque dolorem ad corrupti eligendi quas, ullam porro? Doloribus, consequatur eos molestias eveniet velit accusamus nostrum? Lorem ipsum dolor sit amet consectetur adipisicing elit. Error beatae excepturi eum, odit natus facilis qui rerum</p>
                    <button>Learn more</button>
                </div>

            </div>

            <!--contenitore delle altre ricette secondarie-->
            <div class="other-recipes col-6">
                <div class="row">
                    <div class="col-6" v-for="(image, index) in listaImmagini" :key="index">
                        
                        <div class="overlay">
                            <i class="fa-solid fa-link"></i>
                            <h5>Lunch favourite with salad, Naan and beans</h5>
                        </div>
                        
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

    .overlay{
        background-color: $buttonColor;
        opacity: 0.8;
        position: absolute;
        top: 0;
        right: 0;
        left: 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 20px;
        color: rgba(255,255,255,1);
        visibility: hidden;

        svg{
            background-color: white;
            width: 25px;
            padding: 10px;
            border-radius: 50%;
            color: grey;
        }
    }

    .main-recipe{
        background-color: white;
        padding: 0;
        margin-right: 20px;
        position: relative;

        img{
            width: 100%;
        }

        &:hover .overlay{
            visibility: visible;
            cursor: pointer;
        }

        .overlay{
            left: 0;
            width: 570px;
            height: 377px;
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
            position: relative;
        }

        .overlay{
            left: 12px;
            width: 261px;
            height: 172px;
        }

        &:hover .overlay{
            visibility: visible;
            cursor: pointer;
        }
    }
    
</style>