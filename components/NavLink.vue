<template>
  <NuxtLink :to="link" class="block w-full px-6 py-2 font-medium">
    <font-awesome-icon :icon="icon" class="mr-4" />
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
a.nuxt-link-exact-active {
  @apply bg-black text-white rounded-full;
}
</style>
