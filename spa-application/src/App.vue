<script setup>
import { RouterLink, RouterView } from "vue-router";
import ThemeButtonVue from "./components/ThemeButton.vue";

</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <ThemeButtonVue/>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <h1>Teams</h1>
      </nav>
    </div>
  </header>
  <RouterView/>
</template>

<script>

</script>