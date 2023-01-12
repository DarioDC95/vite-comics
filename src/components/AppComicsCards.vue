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
        <img :src="image" :alt="serie">
        <h4>{{ serie }}</h4>
    </div>
</template>

<style scoped lang="scss">
    .mycard {
        width: 100%;
        margin-bottom: 40px;
        text-transform: uppercase;

        img {
            margin-bottom: 20px;
        };
    }
</style>