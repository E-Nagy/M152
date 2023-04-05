<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/aufgabe1">Aufgabe 1</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style scoped>
nav {
  display: flex;
  justify-content: center;
  padding: 20px 0px;
  background-color: rgb(129, 149, 120);
}

nav a {
  display: block;
  color: rgb(31, 24, 17);
  text-decoration: none;
  margin: 0 10px;
  font-size: 1.5rem;
}
nav a:hover {
  color: rgb(142, 67, 20);
}
</style>
