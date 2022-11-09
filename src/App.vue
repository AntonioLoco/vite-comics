<script>
import AppHeader from './components/AppHeader.vue';
import ProductList from './components/ProductList.vue';
import AppIcons from './components/AppIcons.vue';
import FooterLinks from './components/FooterLinks.vue';
import FooterSocial from './components/FooterSocial.vue';

export default{
  components: {
    AppHeader,
    ProductList,
    AppIcons,
    FooterLinks,
    FooterSocial
  }
}
</script>

<template>
  <AppHeader />
  
  <main>
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
