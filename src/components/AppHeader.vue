<script>
    export default {
        name: 'AppHeader',
        data() {
            return {
                menu: [
                    {
                        label: 'CHARACTERS',
                        url: '#',
                        active: false
                    },
                    {
                        label: 'COMICS',
                        url: '#',
                        active: true
                    },
                    {
                        label: 'MOVIES',
                        url: '#',
                        active: false
                    },
                    {
                        label: 'TV',
                        url: '#',
                        active: false
                    },
                    {
                        label: 'GAMES',
                        url: '#',
                        active: false
                    },
                    {
                        label: 'COLLECTIBLES',
                        url: '#',
                        active: false
                    },
                    {
                        label: 'VIDEOS',
                        url: '#',
                        active: false
                    },
                    {
                        label: 'FANS',
                        url: '#',
                        active: false
                    },
                    {
                        label: 'NEWS',
                        url: '#',
                        active: false
                    },
                    {
                        label: 'SHOP',
                        url: '#',
                        active: false
                    },
                ]
            }
        }
    }
</script>
<template>
    <header>
        <div class="mycontainer">
            <div class="myrow">
                <div class="mycol-md">
                    <img src="../assets/img/dc-logo.png" alt="Logo Favicon">
                </div>
                <div class="mycol-lg">
                    <nav>
                        <ul>
                            <li v-for="(value, index) in menu" :key="index" :class="value.active ? 'active-select' : ''"><a class="underline-none" :href="value.url">{{ value.label }}</a></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins'as *;

header {
    background-color: white;

    .mycontainer {
        @include container-mix;
    
        .myrow {
            display: flex;

            .mycol-md {
                width: 40%;
                display: flex;
                align-items: center;

                img {
                    width: 80px;
                }
            }

            .mycol-lg {
                width: 60%;

                ul {
                    list-style-type: none;
                    display: flex;
                    justify-content: space-between;

                    li {
                        padding: 50px 0;
                        font-size: 12px;
                        font-weight: 600;

                        a {
                            color: black;
                            padding: 20px 0;
                        }
                    }

                    li.active-select {
                        padding-bottom: 45px 0;
                        border-bottom: 5px solid #0282f9;

                        a {
                            color: #0282f9;
                        }
                    }
                }
            }
        }
    }
}
</style>