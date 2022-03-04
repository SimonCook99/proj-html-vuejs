<template>

    <div class="introduction text-center">
        <h4 class="text-uppercase">{{title}}</h4>
        <p>{{description}}</p>
    </div>

</template>

<script>
    export default {
        name:"mainIntroduction",
        props:["title", "description"]
    }
</script>

<style scoped lang="scss">

    .introduction{
        margin-bottom: 55px;

        p{
            width: 50%;
            transform: translate(50%);
            margin-top: 20px;
        }
    }

</style>