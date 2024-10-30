<script setup>
import { items } from "./movies.json";
import MovieCard from "./MovieCard.vue";
/*
 This is an Icon that you can use to represent the stars if you like
 otherwise you could just use a simple ⭐️ emoji, or * character.
*/
// import { StarIcon } from "@heroicons/vue/24/solid";
</script>

<template>
  <!-- This is where your template goes	-->
  <div class="movies">
    <template v-for="movie in items" :key="movie.id">
      <MovieCard :movie="movie"></MovieCard>
    </template>
  </div>
</template>
<style lang="scss" scoped>
.movies {
  display: flex;
  gap: 10px;
}
</style>