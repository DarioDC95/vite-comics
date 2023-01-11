<script>
    export default {
        name: 'AppBody',
        data() {
            return {
                message: '-->Content goes here<--'
            }
        }
    }
</script>

<template>
    <main>
        <div class="mycontainer">
            {{ message }}
        </div>
    </main>
</template>

<style lang="scss">
    @use '../styles/partials/mixins'as *;

    main {
        font-size: 20px;
        font-weight: 600;
        color: white;
        background-color: black;
        padding: 60px 0;

        .mycontainer {
            @include container-mix;
        }
    }
</style>