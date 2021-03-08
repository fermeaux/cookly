<template>
  <section>
    <h1 class="title">
      Les recettes
    </h1>
    <div class="grid grid-cols-3 gap-8">
      <RecipePreview v-for="recipe of recipes" :key="recipe.name" :recipe="recipe" />
    </div>
  </section>
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
