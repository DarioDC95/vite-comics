<script>
  import AppHeader from './components/AppHeader.vue';
  import AppBody from './components/AppBody.vue';
  import AppFooter from './components/AppFooter.vue';
  import dcComics from './data/dc-comics';
  export default {
    components: {
        AppHeader,
        AppBody,
        AppFooter,
        dcComics
    },
    data() {
      return {
        cardDcComics: dcComics
      }
    }
  }
</script>

<template>
  <AppHeader />
  <AppBody :menu="cardDcComics.dcComics"/>
  <AppFooter />
</template>

<style lang="scss">
  @use './styles/general.scss' as *;
</style>