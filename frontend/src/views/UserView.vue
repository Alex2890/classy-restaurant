<template>
  <div class="min-h-screen flex flex-col justify-center items-center bg-[var(--deep-charcoal)] text-[var(--text-white)] px-6 py-12">
    <!-- Title -->
    <h1 class="text-4xl mb-8" style="font-family: var(--font-title);">Noir et Or</h1>

    <!-- Social Sign-In Buttons -->
    <div class="space-y-4 w-full max-w-sm">
      <button class="w-full flex items-center justify-center bg-[var(--darker-charcoal)] text-[var(--text-white)] py-3 rounded-lg hover:bg-[var(--accent-charcoal)] transition">
        <i class="fab fa-google mr-2"></i>
        Continue with Google
      </button>
      <button class="w-full flex items-center justify-center bg-[var(--darker-charcoal)] text-[var(--text-white)] py-3 rounded-lg hover:bg-[var(--accent-charcoal)] transition">
        <i class="fab fa-facebook mr-2"></i>
        Continue with Facebook
      </button>
      <button class="w-full flex items-center justify-center bg-[var(--darker-charcoal)] text-[var(--text-white)] py-3 rounded-lg hover:bg-[var(--accent-charcoal)] transition">
        <i class="fas fa-times mr-2"></i>
        Continue with X
      </button>
    </div>

    <!-- Divider -->
    <div class="my-6 w-full max-w-sm flex items-center">
      <div class="border-t border-[var(--accent-charcoal)] w-full"></div>
      <span class="mx-4 text-[var(--text-white)]">or</span>
      <div class="border-t border-[var(--accent-charcoal)] w-full"></div>
    </div>

    <!-- Email and Password Fields -->
    <form class="space-y-4 w-full max-w-sm">
      <div class="relative">
        <label for="email" class="text-sm text-[var(--text-white)]">Email *</label>
        <input
          type="email"
          id="email"
          placeholder="Enter your email"
          class="mt-1 block w-full px-4 py-2 bg-[var(--darker-charcoal)] text-[var(--text-white)] border border-transparent rounded-lg focus:outline-none focus:border-[var(--primary-gold)] transition"
        />
      </div>

      <div class="relative">
        <label for="password" class="text-sm text-[var(--text-white)]">Password *</label>
        <input
          :type="passwordVisible ? 'text' : 'password'"
          id="password"
          placeholder="Enter your password"
          class="mt-1 block w-full px-4 py-2 bg-[var(--darker-charcoal)] text-[var(--text-white)] border border-transparent rounded-lg focus:outline-none focus:border-[var(--primary-gold)] transition"
        />
        <button
          type="button"
          class="absolute right-3 top-9 text-[var(--text-white)] focus:outline-none"
          @click="togglePasswordVisibility"
        >
          <i :class="passwordVisible ? 'fas fa-eye' : 'fas fa-eye-slash'"></i>
        </button>
      </div>

      <!-- Sign In Button -->
      <button
        type="submit"
        class="w-full py-3 bg-[var(--primary-gold)] text-[var(--secondary-black)] text-lg font-semibold rounded-lg transition transform hover:scale-105 hover:shadow-xl hover:underline"
      >
        Sign In
      </button>
    </form>

    <!-- Links -->
    <div class="mt-6 text-center">
      <a href="#" class="text-sm text-[var(--text-white)] hover:text-[var(--primary-gold)]">Forgot password?</a>
    </div>
    <div class="mt-4 text-center">
      <span class="text-sm text-[var(--text-white)]">New to Noir et Or?</span>
      <a href="#" class="text-sm text-[var(--primary-gold)] hover:underline ml-1">Sign Up</a>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const passwordVisible = ref(false);

const togglePasswordVisibility = () => {
  passwordVisible.value = !passwordVisible.value;
};
</script>

<style scoped>
/* Add any additional styling if needed */
</style>
