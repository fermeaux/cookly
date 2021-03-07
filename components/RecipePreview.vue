<template>
  <NuxtLink class="`text-xl rounded-2xl px-16 py-8" :style="`background-color: ${recipe.preview.color || '#f5f5f5'};`" :to="`/recipes/${recipe.slug}`">
    {{ recipe.name }}
  </NuxtLink>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: ['recipe']
})
</script>
