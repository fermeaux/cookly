<template>
  <nav class="p-8">
    <h2>
      Découvrir
    </h2>
    <ul>
      <li>
        <NuxtLink to="/">
          <font-awesome-icon icon="home" />
          Home
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/">
          <font-awesome-icon icon="search" />
          Recherche
        </NuxtLink>
      </li>
      <li class="active">
        <NuxtLink to="/">
          <font-awesome-icon icon="heart" />
          Pour vous
        </NuxtLink>
      </li>
    </ul>
    <h2>Bibliothèque</h2>
    <ul>
      <li>
        <NuxtLink to="/">
          <font-awesome-icon icon="crown" />
          Chefs
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/">
          <font-awesome-icon icon="star" />
          Favoris
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/">
          <font-awesome-icon icon="utensils" />
          Mes recettes
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
h2 {
    @apply text-xl text-gray-500 opacity-50 uppercase my-4 px-8;
}

li {
    @apply font-medium px-6 mx-2 py-2 my-2 w-full;
}

li.active {
    @apply bg-black text-white rounded-full;
}

li svg {
    @apply mr-4;
}
</style>
