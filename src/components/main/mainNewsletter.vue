<template>
    <section class="newsletter container-fluid">
        <div class="subscription-form">
            
            <h3>Subscribe <span>&</span> Receive a Free eBook</h3>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nisi enim non quas doloribus ullam ab voluptate quis ut</p>
        
            <input type="text" placeholder="insert your email...*">
            <button>Subscribe</button>

            <p>Cras porttitor pellentesque sem eu pretium</p>

        </div>

        <img src="../../assets/img/Yogurt-Nan-600x395.jpg">
        <img src="../../assets/img/Mixed-fruits-400x263.jpg">
        <img src="../../assets/img/r-rachel-park-366508-unsplash-min-400x263.jpg">
        <img src="../../assets/img/r-michelle-tsang-500721-unsplash-min-400x263.jpg">
    </section>
</template>

<script>
    export default {
        name: "mainNewsletter"
    }
</script>

<style scoped lang="scss">

    @import "../SCSS/general.scss";

    section{
        background-image: url("../../assets/img/subscribe-sec-bg.png");
        height: 70vh;
        background-size: cover;
        position: relative;
        margin-top: 100px;

        .subscription-form{
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;

            h3{
                margin-bottom: 20px;
            }

            p{
                margin: 30px 0px;
            }

            span{
                color: $buttonColor;
            }

            button{
                padding: 10px 20px;
            }

            input{
                width: 60%;
                padding: 10px 20px;
                border: 1px solid lightgrey;
                border-radius: 5px;
                margin-right: 50px;
            }
        }

        img{
            width: 25%;
            position: relative;
            top: 100%;
        }
    }
</style>