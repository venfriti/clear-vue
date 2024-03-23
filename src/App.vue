<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
const mobile = false
</script>

<template>
  <nav v-if="mobile === false">
    <div class="space-between">
      <RouterLink to="/">home</RouterLink>
      <RouterLink to="/about">about</RouterLink>
      <RouterLink to="/blog">blog</RouterLink>
    </div>
    <div>
      <img alt="Vue logo" class="logo" src="@/assets/clear-logo.png" width="250" height="auto" />
    </div>
    <div class="space-between">
      <RouterLink to="/shop">shop</RouterLink>
      <RouterLink to="/team">team</RouterLink>
      <RouterLink to="/contact">contact</RouterLink>
    </div>
  </nav>
  <RouterView />
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Barlow:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
* {
  padding: 0;
  margin: 0;
}
nav {
  width: 100%;
  font-family: 'barlow', sans-serif;
  font-size: 14px;
  text-align: center;
  background-color: white;
  padding-top: 2rem;
}
.space-between {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  width: 25vw;
}

@media (min-width: 1024px) {
  .logo {
    margin: 0 2rem 0 0;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 0;
    margin-top: 1rem;
  }
  a {
    text-decoration: none;
    color: black;
    font-weight: 50;
  }
}
</style>
