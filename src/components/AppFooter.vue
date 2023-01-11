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
        <section class="footer-links">
            <div class="mycontainer">
                <div class="myrow">
                    <div class="mycol-lg">
                        <div class="mycard">
                            <div class="margin-right-xs">
                                <div class="dc-comics">
                                    <div class="title">DC COMICS</div>
                                    <ul>
                                        <li>
                                            <a class="underline-none" href="#">Characters</a>
                                        </li>
                                        <li>
                                            <a class="underline-none" href="#">Comics</a>
                                        </li>
                                        <li>
                                            <a class="underline-none" href="#">Movies</a>
                                        </li>
                                        <li>
                                            <a class="underline-none" href="#">TV</a>
                                        </li>
                                        <li>
                                            <a class="underline-none" href="#">Games</a>
                                        </li>
                                        <li>
                                            <a class="underline-none" href="#">Videos</a>
                                        </li>
                                        <li>
                                            <a class="underline-none" href="#">News</a>
                                        </li>
                                    </ul>
                                </div>
                                <div>
                                    <div class="title">SHOP</div>
                                    <ul>
                                        <li>
                                            <a class="underline-none" href="#">Shop DC</a>
                                        </li>
                                        <li>
                                            <a class="underline-none" href="#">Shop DC Collectibles</a>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                            <div class="margin-right-xs">
                                <div class="title">DC</div>
                                <ul>
                                    <li>
                                        <a class="underline-none" href="#">Terms Of Use</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">Privacy policy (New)</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">Ad Choices</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">Advertising</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">Jobs</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">Subscriptions</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">Talent Workshops</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">CPSC Certificates</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">Ratings</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">Shop Help</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">Contact Us</a>
                                    </li>
                                </ul>
                            </div>
                            <div>
                                <div class="title">SITES</div>
                                <ul>
                                    <li>
                                        <a class="underline-none" href="#">DC</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">MAD Magazine</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">DC Kids</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">DC Universe</a>
                                    </li>
                                    <li>
                                        <a class="underline-none" href="#">DC Power Visa</a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="mycol-lg">
                        <div class="mycard">
                            <img src="../assets/img/dc-logo-bg.png" alt="Logo">
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section class="sign-up">
            <div class="mycontainer">
                <div class="myrow">
                    <div class="mycol">
                        <div class="mycard">
                            <button>SIGN-UP NOW!</button>
                        </div>
                    </div>
                    <div class="mycol">
                        <div class="mycard">

                        </div>
                    </div>
                </div>
            </div>
        </section>
    </footer>
</template>

<style scoped lang="scss">
@use '../styles/partials/mixins'as *;
@use '../styles/partials/variables' as *;

.icon-services {
    background-color: $bg-icon-services;
    padding: 50px 0;
    position: relative;
    z-index: 5;

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
                            color: $color-white;
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

.footer-links {
    height: 400px;
    padding-top: 50px;
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;

    .mycontainer {
        @include container-mix;

        .myrow {
            display: flex;
            justify-content: space-between;

            .mycol-lg {
                width: 50%;
                position: relative;
                
                .mycard{
                    display: flex;
                    justify-content: flex-start;

                    img {
                        position: absolute;
                        top: -135px;
                        right: 0;
                        z-index: 1;
                    }

                    .dc-comics {
                        margin-bottom: 20px
                    }

                    .title {
                        color: $color-white;
                        font-size: 20px;
                        font-weight: 500;
                        margin-bottom: 15px;
                    }

                    ul {
                        list-style-type: none;

                        li {
                            margin-bottom: 3px;

                            a {
                                color: $color-grey;
                                font-size: 13px;
                            }
                        }
                    }
                }
            }
        }
    }    
}

.sign-up {
    padding: 50px 0;
    background-color: $bg-brown;
    position: relative;
    z-index: 5;

    .mycontainer {
        @include container-mix;

        .myrow {
            
        }
    } 
}
</style>