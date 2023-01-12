<script>
    export default {
        name: 'AppComicsCards',
        props: {
            image: String,
            cost: String,
            serie: String,
            categorie: String
        },
    }
</script>

<template>
    <div class="mycard">
        <div class="container-img">
            <img :src="image" :alt="serie">
        </div>
        <h4>{{ serie }}</h4>
    </div>
</template>

<style scoped lang="scss">
    .mycard {
        width: 180px;
        margin-bottom: 40px;
        text-transform: uppercase;

        .container-img {
            margin-bottom: 20px;
            height: 180px;
            overflow: hidden;

            img {
                display: block;
            }
        }
    }
</style>