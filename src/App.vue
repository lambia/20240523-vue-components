<script>
export default {
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
    <h1>La Molisana by {{ autore }}</h1>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rerum quisquam, consequatur debitis ipsam fuga molestiae
      deserunt expedita odio a labore et minima? Maxime voluptatum sint sed aperiam, voluptate animi fuga!</p>
</template>