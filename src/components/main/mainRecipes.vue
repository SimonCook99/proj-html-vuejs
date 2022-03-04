<template>
    <section class="popular-recipes">

        <div class="introduction text-center">
            <h4 class="text-uppercase">popular recipes</h4>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius ea deserunt, iure nesciunt rem ratione dignissimos sunt</p>
        </div>


        <div class="row main-row">
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

            <div class="other-recipes col-6">
                <div class="row">
                    <div class="col-6">
                        <img src="../../assets/img/Mixed-fruits-400x263.jpg" alt="mixed fruits">
                    </div>
                    <div class="col-6">
                        <img src="../../assets/img/r-rachel-park-366508-unsplash-min-400x263.jpg" alt="mixed fruits">
                    </div>
                </div>
                <div class="row">
                    <div class="col-6">
                        <img src="../../assets/img/r-michelle-tsang-500721-unsplash-min-400x263.jpg" alt="mixed fruits">
                    </div>
                    <div class="col-6">
                        <img src="../../assets/img/quick-summer-drink-460x295.jpg" alt="mixed fruits">
                    </div>
                </div>
                <div class="row">
                    <div class="col-6">
                        <img src="../../assets/img/r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg" alt="mixed fruits">
                    </div>
                    <div class="col-6">
                        <img src="../../assets/img/perfect-cosmopolitan-460x295.jpg" alt="mixed fruits">
                    </div>
                </div>
                <div class="row">
                    <div class="col-6">
                        <img src="../../assets/img/fi2x-6-460x295.jpg" alt="mixed fruits">
                    </div>
                    <div class="col-6">
                        <img src="../../assets/img/r-brooke-lark-96398-unsplash-min-460x295.jpg" alt="mixed fruits">
                    </div>
                </div>
                
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "mainRecipes"
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

    .introduction{

        margin-bottom: 55px;
        p{
        width: 50%;
        transform: translate(50%);
        margin-top: 20px;
        }
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