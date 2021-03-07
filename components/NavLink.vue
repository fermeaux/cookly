<template>
  <NuxtLink :to="link">
    <font-awesome-icon :icon="icon" />
    {{ label }}
  </NuxtLink>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: ['link', 'label', 'icon']
})
</script>

<style scoped>
a {
  @apply font-medium px-6 py-2 w-full block;
}

a.nuxt-link-exact-active {
  @apply bg-black text-white rounded-full;
}

a svg {
  @apply mr-4;
}
</style>
