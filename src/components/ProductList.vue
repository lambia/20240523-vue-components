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
  <ul>
    <li v-for="tipoDiPasta in products">{{ tipoDiPasta }}</li>
  </ul>
</template>

<style></style>