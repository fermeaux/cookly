<template>
  <section>
    <h1 class="title">
      {{ recipe.name }}
    </h1>
    <div class="grid grid-cols-3 gap-16">
      <div>
        <h2 class="title">
          <font-awesome-icon icon="shopping-basket" class="mr-4" />
          Liste des ingredients
        </h2>
        <ul>
          <li v-for="ingredient of recipe.ingredients" :key="ingredient.id">
            {{ ingredient.name }}
          </li>
        </ul>
      </div>
      <div class="col-span-2">
        <h2 class="title">
          <font-awesome-icon icon="list-ol" class="mr-4" />
          Etapes
        </h2>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  async asyncData ({ params, redirect, $content }) {
    const recipe = await $content(`recipes/${params.id}`).fetch()
    if (recipe == null) { redirect('/errors/404') }

    if (recipe.ingredients == null) { recipe.ingredients = [] }
    for (let index = 0; index < recipe.ingredients.length; index++) {
      const ingredient = recipe.ingredients[index]
      const ingredientTemplate = await $content(`ingredients/${ingredient.id}`).fetch()
      recipe.ingredients[index] = { ...ingredientTemplate, ...ingredient }
    }

    return {
      recipe
    }
  }
})
</script>
