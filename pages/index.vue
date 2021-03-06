<template>
  <div class="container">
    <h1 class="mb-8 text-4xl font-bold">
      Les meilleurs recettes
    </h1>
    <div class="grid grid-cols-3 gap-8">
      <RecipePreview v-for="recipe of recipes" :key="recipe.name" :recipe="recipe" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  async asyncData ({ $content }) {
    const recipes = await $content('recipes').fetch()

    return {
      recipes
    }
  }
})
</script>

<style scoped>
</style>
