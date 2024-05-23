<script>
import AppHeader from './components/AppHeader.vue';
import ProductList from './components/ProductList.vue';

export default {
  components: {
    AppHeader,
    ProductList,
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
    <ProductList />
  </main>
      
</template>