<script setup>
import useAuth from "../composable/useAuth";
const { isAuthenticated, user } = useAuth();
</script>

<template>
  <div
    class="flex flex-col items-center justify-center space-y-12  min-h-screen-nonav"
  >
    <h2
      v-if="!isAuthenticated"
      class="text-6xl tracking-tighter font-extralight"
    >
      Welcome to my website
    </h2>
    <h2 v-else class="text-6xl tracking-tighter font-extralight">
      Welcome master {{ user }}
    </h2>
    <img src="../assets/bgindex.png" alt="Hello BG" />
  </div>
</template>