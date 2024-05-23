<script>
export default {
  data() {
    return {
      products: [
        "Linguine",
        "Spaghetti",
        "Scialatielli",
        "Rigatoni"
      ]
    }
  }
}
</script>

<template>
  <h2>I nostri prodotti</h2>
  <ul>
    <li v-for="tipoDiPasta in products">{{ tipoDiPasta }}</li>
  </ul>
</template>