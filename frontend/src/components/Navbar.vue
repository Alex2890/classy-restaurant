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
          <router-link
            to="/"
            class="text-lg uppercase tracking-wider transition duration-300 hover:text-[var(--hover-darkgold)]"
            :class="{ 'text-[var(--hover-darkgold)] underline': isActiveRoute('/') }"
            style="font-family: var(--font-button);"
          >
            Home
          </router-link>
          <router-link
            to="/menu"
            class="text-lg uppercase tracking-wider transition duration-300 hover:text-[var(--hover-darkgold)]"
            :class="{ 'text-[var(--hover-darkgold)] underline': isActiveRoute('/menu') }"
            style="font-family: var(--font-button);"
          >
            Menu
          </router-link>
          <router-link
            to="/reservations"
            class="text-lg uppercase tracking-wider transition duration-300 hover:text-[var(--hover-darkgold)]"
            :class="{ 'text-[var(--hover-darkgold)] underline': isActiveRoute('/reservations') }"
            style="font-family: var(--font-button);"
          >
            Reservations
          </router-link>
          <router-link
            to="/contact"
            class="text-lg uppercase tracking-wider transition duration-300 hover:text-[var(--hover-darkgold)]"
            :class="{ 'text-[var(--hover-darkgold)] underline': isActiveRoute('/contact') }"
            style="font-family: var(--font-button);"
          >
            Contact
          </router-link>
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
      <router-link
        to="/"
        class="block py-3 text-lg uppercase tracking-wider transition hover:text-[var(--hover-darkgold)]"
        :class="{ 'text-[var(--hover-darkgold)] underline': isActiveRoute('/') }"
        style="font-family: var(--font-button);"
      >
        Home
      </router-link>
      <router-link
        to="/menu"
        class="block py-3 text-lg uppercase tracking-wider transition hover:text-[var(--hover-darkgold)]"
        :class="{ 'text-[var(--hover-darkgold)] underline': isActiveRoute('/menu') }"
        style="font-family: var(--font-button);"
      >
        Menu
      </router-link>
      <router-link
        to="/reservations"
        class="block py-3 text-lg uppercase tracking-wider transition hover:text-[var(--hover-darkgold)]"
        :class="{ 'text-[var(--hover-darkgold)] underline': isActiveRoute('/reservations') }"
        style="font-family: var(--font-button);"
      >
        Reservations
      </router-link>
      <router-link
        to="/contact"
        class="block py-3 text-lg uppercase tracking-wider transition hover:text-[var(--hover-darkgold)]"
        :class="{ 'text-[var(--hover-darkgold)] underline': isActiveRoute('/contact') }"
        style="font-family: var(--font-button);"
      >
        Contact
      </router-link>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";
import { useRoute } from "vue-router";

const mobileMenuOpen = ref(false);

const toggleMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value;
};

// Function to determine if the current route is active
const route = useRoute();
const isActiveRoute = (path) => route.path === path;
</script>
