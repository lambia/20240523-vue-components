<script>
export default {
    name: "ProductCard",
    props: ["prodotto"]
}
</script>

<template>
    <div class="productCard">
        <img :src="prodotto.src" alt="">
        <p>{{ prodotto.titolo }}</p>
        <p>Pasta {{ prodotto.tipo }} che cuoce in {{ prodotto.cottura }} minuti</p>
    </div>
</template>

<style>
.productCard {
    width: 25%;
}
</style>