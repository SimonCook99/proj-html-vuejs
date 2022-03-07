<template>
    <footer>

        <div class="footer-top container">
            <div class="row">
                <div class="col-3">
                    <img src="../assets/img/avada-food-logo-mob-2x.png" alt="logo footer">
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-youtube"></i>
                </div>
                <div class="col-3">
                    <nav>
                        <ul>
                            <li v-for="(item, index) in lista" :key="index">{{item}}</li>
                        </ul>
                    </nav>
                </div>
                <div class="col-3">

                    <h5>Contact</h5>

                    <div class="contact">
                        <i class="fa-solid fa-location-dot"></i>
                        <p>775 New York Ave, Brooklyn, Kings, New York 11203</p>
                    </div>

                    <div class="contact">
                        <i class="fa-solid fa-phone-flip"></i>
                        <p>+ 0100-505-0000</p>
                    </div>

                    <div class="contact">
                        <i class="fa-solid fa-envelope"></i>
                        <p>info@your-domain.com</p>
                    </div>
                    
                </div>
                <div class="col-3">

                    <h5>Get our app</h5>

                    <img src="../assets/img/download-android.png" alt="app android">
                    <img src="../assets/img/download-app-store.png" alt="app apple store">

                    
                    
                </div>
            </div>
        </div>

        <div class="footer-bottom">

            <i class="fa-solid fa-angle-up"></i>

            <p>© Copyright 2012-2020 | Avada Theme by ThemeFusion | All rights Resrved | Powered by Vue CLI</p>

            <div></div>
        </div>
        
        
    </footer>
</template>

<script>
    export default {
        name: "myFooter",
        props:{
            "lista": Array
        }
    }
</script>

<style scoped lang="scss">

    @import "./SCSS/colors.scss";

    footer{
        margin-top: 300px;

        svg{
            margin-top: 30px;
            margin-right: 20px;
            color: grey;
        }

        .col-3{
            position: relative;
            padding: 0px 20px;

            img{
                width: 100%;
                margin-bottom: 20px;
            }

            &:after{
                content: "";
                height: 100%;
                position: absolute;
                top: 0;
                border: 1px dashed $mainButtonColor;
                right: 0;
            }

            li{
                list-style: none;
                margin: 15px 0px;
            }

            h5{
                color: $buttonColor;
                text-transform: uppercase;
                margin-bottom: 30px;
            }

            .contact{
                display: flex;

                svg{
                    margin-top: 0;

                    position: relative;
                    top: 5px;
                }
            }
        }

        .footer-bottom{
            background-color: $mainBackground;
            height: 70px;
            display: flex;
            align-items: center;
            justify-content: space-between;

            svg{
                background-color: #39403e;
                border-radius: 50%;
                padding: 10px;
                color: white;
                margin-top: 10px;
                margin-left: 40px;
            }

            p{
                margin-top: 20px;
            }
        }
    }
</style>