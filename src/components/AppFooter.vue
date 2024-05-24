<script>
export default {
    name: "AppFooter",
    data() {
        return {
            imgVitePublic: "/vite.svg",
            imgVueAssets: "vue.svg"
        }
    },
    methods: {
        //Metodo per elaborare correttamente i percorsi delle immagini
        //Serve quando i file sono sotto assets e il percorso arriva dal data
        //Non serve se le immagini sono in public, o se scriviamo il percorso direttamente da HTML (v. sotto)
        //Il percorso va scritto in una stringa col backtick e dall'esterno ricevo SOLO il nome del file, altrimenti non funzionerà
        getImage(nomefile) {
            return new URL(`../assets/${nomefile}`, import.meta.url);
        }
    }
}
</script>

<template>
    <footer>
        Realizzato con:

        <!-- Immagini in /public: -->
        <!-- Usate un percorso ASSOLUTO, che inizia con "/" -->
        <!-- Funziona sia col percorso scritto da HTML che recuperato dal data -->
        <img class="logo" src="/vite.svg" />
        <img class="logo" :src="imgVitePublic" />
        +
        <!-- Immagini in /src/assets -->
        <!-- Usate un percorso RELATIVO, che quindi inizia con "./" o "../" a seconda dei casi -->
        <!-- Funziona con il percorso scritto direttamente in HTML -->
        <!-- Se invece arriva dal data, dovrete passare per la nostra funzione "getImage" altrimenti in build non vedrete l'immagine -->
        <img class="logo" src="../assets/vue.svg" />
        <img class="logo" :src="getImage(imgVueAssets)" />
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