<template>
    <button
      @click="handleLogin"
      class="px-4 py-2 bg-[var(--primary-gold)] text-[var(--secondary-black)] text-lg font-semibold rounded-lg transition transform hover:scale-105 hover:shadow-xl hover:underline"
      style="font-family: var(--font-button);"
    >
      Log In
    </button>
  </template>
  
<script setup>
import { useRouter } from 'vue-router';

const router = useRouter();
  
const handleLogin = () => {
  router.push('/userview');
};
</script>
  
<style scoped>
  /* Add any additional styling here if needed */
</style>
  