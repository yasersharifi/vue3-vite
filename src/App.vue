<template>
  <ul >
    <li v-for="(item, index) in pages" :key="index">
      <router-link :to="item.path">{{item.title}}</router-link>
    </li>
  </ul>
  <router-view></router-view>
</template>

<script setup lang="ts">
  import { ref } from 'vue'
  const pages = ref([
    {
      title: 'Home',
      path: '/'
    },
    {
      title: 'About',
      path: '/about'
    }
  ])
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
