<template>
    <section class="culinary-collection">

        <mainIntroduction 
            title="culinary collection"
            description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius ea deserunt, iure nesciunt rem ratione dignissimos sunt"
        />

        <div class="row card-container">
            <div class="col-3">
                <img src="../../assets/img/drinks-recipes.png" alt="drinks">
                <h5>Drinks</h5>
            </div>
            <div class="col-3">
                <img src="../../assets/img/soups-recipes.png" alt="drinks">
                <h5>Soups</h5>
            </div>
            <div class="col-3">
                <img src="../../assets/img/baking-recipes.png" alt="drinks">
                <h5>Bakery</h5>
            </div>
            <div class="col-3">
                <img src="../../assets/img/dinner-recipes.png" alt="drinks">
                <h5>Dinner</h5>
            </div>

            <div class="col-3">
                <img src="../../assets/img/healthy-recipes.png" alt="drinks">
                <h5>Healthy</h5>
            </div>
            <div class="col-3">
                <img src="../../assets/img/drinks-recipes.png" alt="drinks">
                <h5>Staff picks</h5>
            </div>
            <div class="col-3">
                <img src="../../assets/img/premium-recipes.png" alt="drinks">
                <h5>Appetisers</h5>
            </div>
            <div class="col-3">
                <img src="../../assets/img/quick-easy-recipes.png" alt="drinks">
                <h5>Quick & easy</h5>
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
        }
    }
</script>

<style scoped lang="scss">
    .culinary-collection{
        margin-top: 150px;
    }

    
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
    }

</style>