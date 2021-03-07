<template>
  <div>
    {{ recipe.name }}
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  async asyncData ({ params, redirect, $content }) {
    const recipe = await $content(`recipes/${params.id}`).fetch()

    if (recipe == null) { redirect('/errors/404') }

    return {
      recipe
    }
  }
})
</script>
