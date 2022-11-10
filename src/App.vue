<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbotron from './components/AppJumbotron.vue';
import ProductList from './components/ProductList.vue';
import AppIcons from './components/AppIcons.vue';
import FooterLinks from './components/FooterLinks.vue';
import FooterSocial from './components/FooterSocial.vue';

export default{
  components: {
    AppHeader,
    AppJumbotron,
    ProductList,
    AppIcons,
    FooterLinks,
    FooterSocial
  },
  methods: {
    getImagePath(imgPath){
      return new URL(imgPath, import.meta.url).href;
    }
  }
}
</script>

<template>
  <AppHeader />
  
  <main>
    <AppJumbotron :imgUrl="getImagePath('./assets/img/jumbotron.jpg')" :nameSection="'current series'" />
    <ProductList />
    <AppIcons />
  </main>
  
  <footer>
    <FooterLinks />
    <FooterSocial />
  </footer>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
