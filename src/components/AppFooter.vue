<template>
    <footer>
        Realizzato con: 
        <!-- Percorso ASSOLUTO: Immagine presa dalla cartella /public -->
        <img class="logo" src="/vite.svg" />
        +
        <!-- Percorso RELATIVO: Immagine presa dalla cartella /src/assets -->
        <img class="logo" src="../assets/vue.svg" />
        <a v-for="link in links" :href="link.url">{{ link.text }}</a>
    </footer>
</template>

<style scoped>
footer {
    background-color: #444;
    padding: 1rem;
}

img.logo {
    height: 1rem;
    transition: all 300ms;
}
img.logo:hover {
    transform: scale(1.75);
}
</style>