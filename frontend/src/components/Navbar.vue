<template>
  <nav class="bg-black text-[var(--primary-gold)] fixed w-full top-0 z-50 shadow-lg border-b border-[var(--primary-gold)]">
    <div class="max-w-7xl mx-auto px-6 lg:px-12">
      <div class="flex justify-between items-center h-20">
        <!-- Logo / Brand Name -->
        <div class="flex items-center">
          <h1 class="text-4xl font-extrabold tracking-wide" style="font-family: var(--font-title);">
            Noir et Or
          </h1>
        </div>

        <!-- Desktop Navigation -->
        <div class="hidden md:flex space-x-8">
          <a href="#" class="text-lg uppercase tracking-wider transition duration-300 hover:text-[var(--hover-darkgold)]" style="font-family: var(--font-button);">
            Home
          </a>
          <a href="#" class="text-lg uppercase tracking-wider transition duration-300 hover:text-[var(--hover-darkgold)]" style="font-family: var(--font-button);">
            Menu
          </a>
          <a href="#" class="text-lg uppercase tracking-wider transition duration-300 hover:text-[var(--hover-darkgold)]" style="font-family: var(--font-button);">
            Reservations
          </a>
          <a href="#" class="text-lg uppercase tracking-wider transition duration-300 hover:text-[var(--hover-darkgold)]" style="font-family: var(--font-button);">
            Contact
          </a>
        </div>

        <!-- Mobile Menu Button -->
        <div class="md:hidden">
          <button @click="toggleMenu" class="text-3xl hover:text-[var(--hover-darkgold)] focus:outline-none">
            ☰
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu (Hidden by Default) -->
    <div v-if="mobileMenuOpen" class="md:hidden absolute top-20 left-0 w-full bg-black text-center py-4 shadow-lg border-t border-[var(--primary-gold)]">
      <a href="#" class="block py-3 text-lg uppercase tracking-wider transition hover:text-[var(--hover-darkgold)]" style="font-family: var(--font-button);">
        Home
      </a>
      <a href="#" class="block py-3 text-lg uppercase tracking-wider transition hover:text-[var(--hover-darkgold)]" style="font-family: var(--font-button);">
        Menu
      </a>
      <a href="#" class="block py-3 text-lg uppercase tracking-wider transition hover:text-[var(--hover-darkgold)]" style="font-family: var(--font-button);">
        Reservations
      </a>
      <a href="#" class="block py-3 text-lg uppercase tracking-wider transition hover:text-[var(--hover-darkgold)]" style="font-family: var(--font-button);">
        Contact
      </a>
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
