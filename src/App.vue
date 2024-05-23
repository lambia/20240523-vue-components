<script>
import AppHeader from './components/AppHeader.vue';
import ProductList from './components/ProductList.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    ProductList,
    AppFooter
  },
  data() {
    return {
      autore: "Luca Lambiase"
    }
  },
  methods: {
    welcome() {
      console.log("Benvenuto nell'applicazione di La Molisana, sviluppata da ", this.autore);
    }
  },
  mounted() {
    this.welcome();
  }
}
</script>

<template>
  <AppHeader />
  <!-- <a href="google.it">Link non stilizzato in header</a> -->

  <main>
    <h1>La Molisana by {{ autore }}</h1>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
    <div class="wrapper">
      <ProductList />
    </div>
  </main>

  <AppFooter />
      
</template>

<style scoped>
.wrapper {
  padding: 1rem 0;
}
</style>