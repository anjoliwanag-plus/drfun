<template>
  <v-app>
    <v-main>
      <NavBar />
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script setup lang="ts">
import NavBar from '@/components/NavBar.vue'
</script>
