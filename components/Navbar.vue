<template>
  <nav class="p-8">
    <h2>Découvrir</h2>
    <ul>
      <li>
        <NavLink link="/" label="Home" icon="home" />
      </li>
      <li>
        <NavLink link="/search" label="Recherche" icon="search" />
      </li>
      <li>
        <NavLink link="/suggestions" label="Pour vous" icon="heart" />
      </li>
    </ul>
    <h2>Bibliothèque</h2>
    <ul>
      <li>
        <NavLink link="/chiefs" label="Chefs" icon="crown" />
      </li>
      <li>
        <NavLink link="/favorites" label="Favoris" icon="star" />
      </li>
      <li>
        <NavLink link="/recipes" label="Mes recettes" icon="utensils" />
      </li>
    </ul>
  </nav>
</template>

<style scoped>
h2 {
  @apply text-xl text-gray-500 uppercase my-4 px-8;
}

li {
  @apply mx-2 my-2;
}
</style>
