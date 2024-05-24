<script>
import ProductCard from "./ProductCard.vue";

export default {
  components: {
    ProductCard
  },
  data() {
    return {

      products: [
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
          titolo: "N.4 Spaghetto Quadrato Bucato",
          tipo: "lunga",
          cottura: 6,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
          titolo: "N.5 Fettuccine",
          tipo: "lunga",
          cottura: 13,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/6-linguine.jpg",
          titolo: "N.6 Linguine",
          tipo: "lunga",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/7-mezze-linguine.jpg",
          titolo: "N.7 Mezze Linguine",
          tipo: "lunga",
          cottura: 11,
        }
      ]
    }
  }
}
</script>

<template>

  <!-- Versione iniziale: uso un semplice ciclo -->
  <h2>I nostri prodotti</h2>
  <h3>Questi prodotti sono stampati direttamente qui, a km0</h3>

  <div class="products">
    <div v-for="elemento in products" class="productCard">
      <img :src="elemento.src" alt="">
      <p>{{ elemento.titolo }}</p>
      <p>Pasta {{ elemento.tipo }} che cuoce in {{ elemento.cottura }} minuti</p>
    </div>
  </div>

  <!-- Versione di test: creo un componente e gli passo un dato, a mano -->
  <h2>I nostri stessi prodotti</h2>
  <h3>Stampati però da un componente figlio, passandoli a mano.</h3>
  <h4>Questo codice fa sanguinare altri programmatori dagli occhi, ma è utile per testare un componente al volo</h4>

  <div class="products">
    <ProductCard :prodotto="products[0]" />
    <ProductCard :prodotto="products[2]" />
  </div>

  <!-- Versione finale: uso il componente, in un ciclo -->
  <h2>Ancora una volta i prodotti</h2>
  <h3>Finalmente stampati grazie a un ciclo che passa i dati al componente figlio.</h3>

  <div class="products">
    <ProductCard v-for="elemento in products" :prodotto="elemento" />
  </div>

</template>

<style>
h2 {
  font-size: 2rem;
  margin-top: 2rem;
  margin-bottom: 0.5rem;
}

.products {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.productCard {
  width: 25%;
  padding: 1rem;
}

.productCard>img {
  width: 100%;
}
</style>