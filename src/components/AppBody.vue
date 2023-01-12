<script>
    import AppComicsCards from './AppComicsCards.vue';
    import dcComics from '../data/dc-comics';
    export default {
        name: 'AppBody',
        components: {
            AppComicsCards,
            dcComics
        },
        data() {
            return {
                dcComicsCards: dcComics,
                message: '-->Content goes here<--'
            }
        },
    }
</script>

<template>
    <main>
        <section class="jumbotron">
            <div class="mycontainer">
                <div class="current-series">CURRENT SERIES</div>
            </div>
        </section>
        <section class="main-content">
            <div class="mycontainer">
                <div class="myrow">
                    <div v-for="(value, index) in dcComicsCards.dcComics" :key="index" class="mycol-sm">
                        <AppComicsCards :image="value.thumb" :serie="value.series"/>
                    </div>
                </div>
                <div class="button">
                    <button>LOAD MORE</button>
                </div>
            </div>
        </section>
    </main>
</template>

<style scoped lang="scss">
    @use '../styles/partials/mixins' as *;
    @use '../styles/partials/variables' as *;

    main {
        font-weight: 600;
        color: white;
        background-color: $bg-black;

        .jumbotron {
            height: 400px;
            background-image: url('../assets/img/jumbotron.jpg');
            background-repeat: no-repeat;
            background-size: cover;

            .mycontainer {
                @include container-mix;
                height: 100%;
                position: relative;

                .current-series {
                    background-color: $bg-icon-services;
                    display: inline-block;
                    padding: 10px 30px;
                    font-size: 20px;
                    position: absolute;
                    bottom: 0;
                    transform: translateY(50%);
                }
            }
        }

        .main-content {
            padding-top: 50px;
            padding-bottom: 20px;

            .mycontainer {
                @include container-mix;
                padding: 0 20px;

                .myrow {
                    display: flex;
                    justify-content: space-between;
                    flex-wrap: wrap;
                }

                .button {
                    text-align: center;

                    button {
                        padding: 15px 20px ;
                        border: 3px solid $color-blue;
                        background-color: $color-blue;
                        font-weight: 600;
                        font-size: 17px;
                        color: $color-white;
                        cursor: pointer;
        
                        &:hover {
                            border: 3px solid $color-white;
                            color: $color-white;
                        }
        
                        &:active {
                            color: $bg-black;
                            background-color: $color-white;
                            border: 3px solid $color-blue;
                        }
                    }
                }
            }
        }
    }
</style>