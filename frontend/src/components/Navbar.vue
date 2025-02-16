<template>
    <nav class="bg-black text-gold fixed w-full top-0 z-50 shadow-lg border-b border-gold">
      <div class="max-w-7xl mx-auto px-6 lg:px-12">
        <div class="flex justify-between items-center h-20">
          <!-- Logo / Brand Name -->
          <div class="flex items-center">
            <h1 class="text-4xl font-extrabold tracking-wide font-cursive">Noir et Or</h1>
          </div>
  
          <!-- Desktop Navigation -->
          <div class="hidden md:flex space-x-8">
            <a href="#" class="text-gold font-cursive hover:text-white transition duration-300 text-lg uppercase tracking-wider">Home</a>
            <a href="#" class="text-gold font-cursive hover:text-white transition duration-300 text-lg uppercase tracking-wider">Menu</a>
            <a href="#" class="text-gold font-cursive hover:text-white transition duration-300 text-lg uppercase tracking-wider">Reservations</a>
            <a href="#" class="text-gold font-cursive hover:text-white transition duration-300 text-lg uppercase tracking-wider">Contact</a>
          </div>
  
          <!-- Mobile Menu Button -->
          <div class="md:hidden">
            <button @click="toggleMenu" class="text-gold hover:text-white focus:outline-none text-3xl">
              ☰
            </button>
          </div>
        </div>
      </div>
  
      <!-- Mobile Menu (Hidden by Default) -->
      <div v-if="mobileMenuOpen" class="md:hidden absolute top-20 left-0 w-full bg-black text-center py-4 shadow-lg border-t border-gold">
        <a href="#" class="block py-3 text-gold font-cursive hover:text-white text-lg uppercase tracking-wider transition">Home</a>
        <a href="#" class="block py-3 text-gold font-cursive hover:text-white text-lg uppercase tracking-wider transition">Menu</a>
        <a href="#" class="block py-3 text-gold font-cursive hover:text-white text-lg uppercase tracking-wider transition">Reservations</a>
        <a href="#" class="block py-3 text-gold font-cursive hover:text-white text-lg uppercase tracking-wider transition">Contact</a>
      </div>
    </nav>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  const mobileMenuOpen = ref(false);
  
  const toggleMenu = () => {
    mobileMenuOpen.value = !mobileMenuOpen.value;
  };
  </script>
  
  <style scoped>
  /* Define Gold Color */
  .text-gold {
    color: #d4af37; /* Rich Gold */
  }
  
  .border-gold {
    border-color: #d4af37;
  }
  
  /* Custom Font (Cursive) */
  .font-cursive {
    font-family: "Dancing Script", cursive;
  }
  
  /* Smooth Transition */
  .text-gold:hover {
    transition: color 0.3s ease-in-out;
  }
  </style>
  