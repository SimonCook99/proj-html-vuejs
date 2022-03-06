<template>
    <section class="social-blog">

        <mainIntroduction 
            title="Farm to table"
            description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius ea deserunt, iure nesciunt rem ratione dignissimos sunt"
            :leftAlign="true"
        />

        <button class="start">Read our blog <i class="fa-solid fa-map-location"></i> </button>

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

                <button id="load" class="grey">Load more posts</button>
                
            </div>
            <!--fine prima macrocolonna-->

            <!--inizio seconda macrocolonna-->
            <div class="col-4">

                <div class="recipes">
                    <img class="recipes" src="../../assets/img/cadvert.jpg" alt="ad recipes">
                    <h4>View our latest recipes</h4>
                </div>

                <div class="city-guide">
                    <img src="../../assets/img/singapore-featured-image-400x263.jpg" alt="">

                    <h3>City Guide: Singapore</h3>

                    <button>
                        <i class="fa-solid fa-earth-americas"></i>
                        <span class="text-uppercase">View all city guides</span>
                    </button>

                    <hr class="my-5">
                </div>


                <div class="social">
                    
                    <div class="search">
                        <i class="fa-solid fa-magnifying-glass"></i>
                        <input type="text" placeholder="Search...">
                    </div>

                    <div class="follow">
                        <h6>Follow us</h6>

                        <button class="grey"><i class="fa-brands fa-facebook-f"></i></button>
                        <button class="grey"><i class="fa-brands fa-instagram"></i></button>
                        <button class="grey"><i class="fa-brands fa-twitter"></i></button>
                        <button class="grey"><i class="fa-brands fa-youtube"></i></button>
                        <button class="grey"><i class="fa-brands fa-pinterest-p"></i></button>
                    </div>

                    <div class="filter">
                        <button class="bg-white">Popular</button>
                        <button class="grey">recent</button>
                    </div>
                    

                </div>
                
                

                
            </div>
            <!--fine seconda macrocolonna-->

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

    img{
        width: 85%;
    }

    .social-blog{
        position: relative;

        button.start{
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

        #load{
            position: relative;
            width: calc(100% - 50px);
            margin-left: 15px;
            color: black;
        }


        .col-4{
            text-align: center;

            .recipes{
                margin-bottom: 30px;
                position: relative;

                h4{
                    position: absolute;
                    top: 37%;
                    left: 50%;
                    transform: translate(-50%);
                    padding: 0px 30px;
                    text-transform: uppercase;
                }
            }

            .city-guide{
                position: relative;

                h3{
                    position: absolute;
                    top: 40%;
                    left: 8%;
                    color: white;
                    background-color: rgba(0,0,0,0.5);
                    padding: 10px;
                    font-size: 20px;
                }

                button, hr{
                    position: relative;
                    width: 85%;
                }
                hr{
                    left: 8%;
                }
            }
        }

        .social{

            .search{
                position: relative;

                svg{
                    position: absolute;
                    top: 50%;
                    transform: translate(0, -50%);
                    left: 40px;
                }
            }
            
            input{
                width: 85%;
                border: 0;
                padding: 10px;
                padding-left: 50px;
                border-radius: 10px;
                border: 2px solid $mainButtonColor;

                &:before{
                    display: inline-block;
                    text-rendering: auto;
                    -webkit-font-smoothing: antialiased;
                    font: var(--fa-font-solid);
                    content: "f002";
                }
            }

            .follow{
                text-align: left;
                position: relative;
                left: 8%;
                margin-top: 40px;

                button.grey{
                    padding: 5px 10px;
                    background-color: #edede7;
                    margin-top: 20px;
                    color: grey;
                    margin-right: 15px;
                    border-radius: 5px;
                    border: 2px solid $mainButtonColor;
                }
            }

            .filter{
                button{
                    color: black;
                    margin-top: 40px;
                    width: calc(85% / 2);
                    padding: 10px 20px;
                }
            }
            
            
        }
    }

    
    
</style>