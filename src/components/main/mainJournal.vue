<template>
    <section class="journal">
        <h3 class="title">Foodie journal</h3>
                
        <div class="row">
            <div class="col-4">
                <img src="../../assets/img/single-post-img3-400x263.jpg">

                <!--contenitore overlay per l'effetto di hover-->
                <div class="overlay">
                    <i class="fa-solid fa-link"></i>
                    <h5>Food corner: Top Japanese Restaurants For Sushi</h5>
                </div>

                <h4>Food corner: Top Japanese Restaurants For Sushi</h4>
                <p>by Admin, March 25th, 2019</p>
            </div>
            <div class="col-4">
                <img src="../../assets/img/fi-roundup-400x263.jpg">

                <div class="overlay">
                    <i class="fa-solid fa-link"></i>
                    <h5>Roundup: My new favourite Recipes for Healthy Living</h5>
                </div>

                <h4>Roundup: My new favourite Recipes for Healthy Living</h4>
                <p>by Admin, March 25th, 2019</p>
            </div>
            <div class="col-4">
                <img src="../../assets/img/fi-toasts-400x263.jpg">

                <div class="overlay">
                    <i class="fa-solid fa-link"></i>
                    <h5>Why These Toasts with Tea are My new Favourite</h5>
                </div>

                <h4>Why These Toasts with Tea are My new Favourite</h4>
                <p>by Admin, March 25th, 2019</p>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name:"mainJournal"
    }
</script>

<style scoped lang="scss">

    @import "../SCSS/colors.scss";

    .journal{
            text-align: center;
            background-color: white;
            padding: 0px 20px;
            position: relative;
            top: -80px;

            h3.title{
                position: relative;
                padding: 20px;
                font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

                &:before, &:after{ //creazione delle linee prima e dopo il titolo h3
                    content: "";
                    position: absolute;
                    width: 40%;
                    top: 50%;
                    height: 1px;
                    background: $mainBackground; 
                }
                &:after{
                    left: 60%;
                }
                &:before{
                    left: 0;
                }
            }
        }

        .col-4{
            position: relative;

            &:hover .overlay{
                visibility: visible;
            }

            .overlay{
                background-color: $buttonColor;
                opacity: 0.8;
                position: absolute;
                top: 0;
                right: 0;
                left: 12px;
                width: 343px;
                height: 225px;
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
        }

        img{
            max-width: 100%;
            margin-bottom: 15px;
        }

</style>