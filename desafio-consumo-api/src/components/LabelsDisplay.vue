<template>
    <div class="container">
        <CountriesLabel />
        <AnimeLabel />
        <MangasLabel />
        <RecommendationAnimeLabel />
    </div>
</template>

<script setup>
import CountriesLabel from './CountriesLabel.vue'
import AnimeLabel from './AnimeLabel.vue'
import MangasLabel from './MangasLabel.vue'
import RecommendationAnimeLabel from './RecommendationAnimeLabel.vue';
</script>

<style scoped>
.container{
    display: flex;
    flex-direction: row;
    align-items: top;
    justify-content: center;
    margin-top: 50px;
    gap: 20px;
}
</style>