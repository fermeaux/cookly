<template>
  <div :class="`rounded-2xl px-16 py-8 bg-${recipe.preview.color || 'white'}`">
    {{ recipe.name }}
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: ['recipe']
})
</script>
