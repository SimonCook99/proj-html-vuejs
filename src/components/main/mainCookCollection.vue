<template>
    <section class="culinary-collection">

        <mainIntroduction 
            title="culinary collection"
            description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius ea deserunt, iure nesciunt rem ratione dignissimos sunt"
        />

        <div class="row card-container">
            <div class="col-3" v-for="(image,index) in imagesList" :key="index">
                <img :src="require('../../assets/img/' + image.url)" :alt="image">
                <h5 class="text-uppercase">{{image.type}}</h5>
            </div>
            
        </div>
    </section>
</template>

<script>

    import mainIntroduction from "./partials/mainIntroduction.vue";

    export default {
        name: "mainCookCollection",
        components:{
            mainIntroduction
        },
        props: {
            imagesList: Array
        }
    }
</script>

<style scoped lang="scss">
    
    @import "../SCSS/colors.scss";

    .card-container .col-3{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background-color: white;
        margin: 20px;
        width: calc(25% - 40px);
        padding: 20px 0px;

        img{
            width: 50%;
        }

        h5{
            width: 90%;
            height: 50px;
            text-align: center;
            margin: 0px 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        &:hover h5{
            background-color: $buttonColor;
            color: white;
            cursor: pointer;
        }
    }

</style>