<script>

export default {
    data() {
        return {
            links: [
                {
                    text: "Home",
                    url: "#home",
                },
                {
                    text: "Prodotti",
                    url: "#products",
                },
                {
                    text: "Chi Siamo",
                    url: "#who",
                },
                {
                    text: "Contatti",
                    url: "#contacts",
                },
            ],
        }
    }
}

</script>

<template>
    <header>
        <a v-for="link in links" :href="link.url">{{ link.text }}</a>
    </header>
</template>

<style scoped>
header {
    background: #444;
    padding: 1rem;
}

a {
    color: aquamarine;
    text-decoration: none;
    margin: 0 2rem;
}
</style>