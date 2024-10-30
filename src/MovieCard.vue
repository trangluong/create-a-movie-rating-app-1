<template>
  <div class="movie" > 
    <img class="movie-img" :src="movie.image"/>
    <div class="movie-content ">
      <div class="movie-title">{{ movie.name }}</div>
      <div class="movie-genres" >
        <div class="tag" v-for="gen in movie.genres" :key="gen"> {{ gen }}</div>
      </div>
      <div class="movie-desc">{{ movie.description }}</div>
      <div class="movie-rating">
        <span>{{ `Rating ${movie.rating}/5` }}</span>
        <div class="stars">
          <div v-for="s in movie.rating" :key="s" class="star">
            ⭐️
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script setup>
const props = defineProps({
  movie: Object
})
</script>

<style lang="scss" scoped>
.movie {
  width: 300px;
  height: 550px;

  .movie-img {
    height: 60%;
    width: 100%;
  }
  .movie-content {
    flex-grow: 1;
    padding: 10px 15px;
    background-color: white;
    .movie-genres {
      display: flex;
      flex-direction: row;
      gap: 10px;
    }
    .tag {
      padding: 2px;
      background-color: blueviolet;
      border-radius: 7px;
    }
    .movie-rating {
      display: flex;
      gap: 5px;
    }
    .stars {
      display: flex;
      gap: 5px;
    }
  }
}
</style>