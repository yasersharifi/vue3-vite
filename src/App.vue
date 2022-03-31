<template>
  <div class="bg-orange-50 w-full min-h-screen">
      <ul class="container mx-auto py-6  flex items-center gap-3 w-full">
      <li v-for="(item, index) in pages" :key="index">
        <router-link :to="item.path">{{item.title}}</router-link>
      </li>
    </ul>
    <router-view></router-view>
  </div>
</template>

<script setup lang="ts">
  import { Ref } from 'vue'

  const pages: Ref<[{title: String, path: String}]> = ([
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

</style>
