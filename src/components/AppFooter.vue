<script>
    export default {
        name: 'AppFooter',
        data() {
            return {
                icons: [
                    {
                        url: '/src/assets/img/buy-comics-digital-comics.png',
                        title: 'DIGITAL COMICS',
                    },
                    {
                        url: '/src/assets/img/buy-comics-merchandise.png',
                        title: 'DC MERCHANDISE',
                    },
                    {
                        url: '/src/assets/img/buy-comics-subscriptions.png',
                        title: 'SUBSCRIPTION',
                    },
                    {
                        url: '/src/assets/img/buy-comics-shop-locator.png',
                        title: 'COMIC SHOP LOCATOR',
                    },
                    {
                        url: '/src/assets/img/buy-dc-power-visa.svg',
                        title: 'DC POWER VISA',
                    },
                ]
            }
        }
    }
</script>

<template>
    <footer>
        <section class="icon-services">
            <div class="mycontainer">
                <div class="myrow">
                    <div v-for="(value, index) in icons" :key="index" class="mycol-sm">
                        <div class="mycard">
                            <img :src="value.url" :alt="value.title">
                            <div>
                                <span>{{ value.title }}</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section class="">
            
        </section>
    </footer>
</template>

<style scoped lang="scss">
@use '../styles/partials/mixins'as *;

.icon-services {
    background-color: #0282f9;
    padding: 50px 0;

    .mycontainer {
        @include container-mix;
    
        .myrow {
            width: 100%;
            display: flex;
            justify-content: space-around;

            .mycol-sm {
                display: flex;
                align-items: center;

                .mycard {
                    display: flex;
                    align-items: center;

                    div {

                        span {
                            font-size: 14px;
                            color: white;
                        }
                    }
                    
                    img {
                        width: 45px;
                        margin-right: 10px;
                    }
                }
            }
        }
    }
}
</style>