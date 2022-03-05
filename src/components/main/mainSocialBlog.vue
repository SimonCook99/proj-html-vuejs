<template>
    <section class="social-blog">

        <mainIntroduction 
            title="Farm to table"
            description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius ea deserunt, iure nesciunt rem ratione dignissimos sunt"
            :leftAlign="true"
        />

        <button>Read our blog <i class="fa-solid fa-map-location"></i> </button>

        <!--contenitore principale-->
        <div class="row">

            <!--divisione in 2 macrocolonne, la più grande contiene le varie cards, mentre la più piccola contiene tutta la sezione social sulla destra-->
            <div class="col-8">

                <div class="main-card">
                    <img src="../../assets/img/single-post-img3-600x395.jpg">
                
                    <div class="info">
                        <h4>Food Corner: Top Japanese restaurants for Sushi</h4>
                        <p>by Admin, March 25th 2019</p>

                        <hr>

                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis, nulla eum. Culpa tempora expedita cumque dolorem ad corrupti eligendi quas, ullam porro? Doloribus, consequatur eos molestias eveniet velit accusamus nostrum? Lorem ipsum dolor sit amet consectetur adipisicing elit. Error beatae excepturi eum, odit natus facilis qui rerum</p>
                    
                        <div class="final-section">
                            <p> Read more <i class="fa-solid fa-angle-right"></i></p>

                            <p> <i class="fa-regular fa-comments"></i> 0</p>
                        </div>
                    
                    </div>
                </div>

                <div class="other-cards row">

                    <!--stampa dinamica delle carte tramite la prop passata da myMain-->
                    <div class="card col-6" v-for="(card, index) in cardsList" :key="index">
                        <img :src="require('../../assets/img/' + card.url)">
                    

                        <h4>{{card.title}}</h4>
                        <p>{{card.author}}</p>
                    </div>

                </div>
                
            </div>

            <div class="col-4">
                
            </div>
        </div>

    </section>
</template>

<script>

    import mainIntroduction from "./partials/mainIntroduction.vue";

    export default {
        name: "mainSocialBlog",
        components:{
            mainIntroduction
        },
        props:{
            "cardsList": Array
        }
    }
</script>

<style scoped lang="scss">

    @import "../SCSS/general.scss";

    .social-blog{
        position: relative;

        button{
            position: absolute;
            top: 0;
            right: 0;
            padding: 10px 20px;

            svg{
                margin: 0px 10px;
            }
        }

        .main-card{
            background-color: white;
            padding: 0;
            margin-right: 20px;

            img{
                width: 100%;
            }

            .final-section{
                display: flex;
                justify-content: space-between;
                margin-top: 25px;
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
        }

        .other-cards{
            text-align: center;
            margin: 20px;
            margin-left: 0;

            .card{
                width: calc(50% - 30px);
                margin: 15px;
                background-color: white;
                border: 0;
                padding-bottom: 15px;

                h4,p{
                    padding: 10px 10px 0px 10px;
                }
            }
        }
    }

    
    
</style>