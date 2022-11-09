<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <div class="container">
    <div class="card">
      <input 
        @change="toogleTheme"
        id="checkbox"
        type="checkbox"
        class="switch-checkbox"
      />
      <label for="checkbox" class="switch-label">
        <span>D</span>
        <span>L</span>
        <div
          class="switch-toogle"
          :class="{'switch-toogle-checked': userTheme === 'dark-theme'}"  
        ></div>
      </label>"
    </div>
  </div>
  <RouterView />
</template>

<script>
export default {
  mounted() {
    const initUSerTheme = this.getMediaPreference();
    this.setTheme(initUSerTheme);
  },

  data() {
    return {
      userTheme: "light-theme",
    };
  },
};
</script>
