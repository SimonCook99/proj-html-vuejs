<template>
    <section class="container-fluid">
        <div class="daily-topic">
            <button>Today's pick</button>
            <h1>Food corner: Top Japanese Restaurants For Sushi</h1>
            <p class="date">March 25, 2019</p>
        </div>
    </section>
</template>

<script>
    export default {
        name: "myJumbotron"
    }
</script>

<style scoped lang="scss">

    section{
        background-image: url("../assets/img/single-post-img3.jpg");
        background-size: cover;
        height: 700px;
        position: relative;

        display: flex;
        align-items: center;
        justify-content: center;
    }

    .daily-topic{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background-color: white;
        padding: 20px 55px;
        border-radius: 15px;

        width: 45%;
        text-align: center;

        h1{
            padding-bottom: 20px;
            font-size: 35px;
        }

        button{
            padding: 10px 20px;
            border-radius: 10px;
            position: relative;
            bottom: 50px;
        }
    }
</style>