<template>

    <div class="introduction" :class="leftAlign ? 'text-start' : 'text-center'">
        <h4 class="text-uppercase">{{title}}</h4>
        <p>{{description}}</p>
    </div>

</template>

<script>
    export default {
        name:"mainIntroduction",
        props:["title", "description", "leftAlign"]
    }
</script>

<style scoped lang="scss">

    .introduction{
        margin-top: 150px;
        margin-bottom: 55px;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

        p{
            width: 50%;
            margin-top: 20px;
        }
        
        &.text-center p{
            transform: translate(50%);
        }
    }

</style>