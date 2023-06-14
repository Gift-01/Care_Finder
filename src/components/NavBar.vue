<template>
  <nav
    class="bg-white h-[100px]"
    style="box-shadow: 0px 4px 4px rgba(14, 61, 183, 0.15)"
  >
    <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
      <div class="relative flex items-center justify-between h-16">
        <!-- Hamburger button -->
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <button
            @click="isOpen = !isOpen"
            type="button"
            class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:bg-gray-700 focus:text-white transition duration-150 ease-in-out"
            :aria-expanded="isOpen ? 'true' : 'false'"
          >
            <span class="sr-only">Open main menu</span>
            <svg
              class="block h-6 w-6"
              viewBox="0 0 24 24"
              stroke="currentColor"
              fill="none"
            >
              <path
                :class="{ hidden: isOpen, 'inline-flex': !isOpen }"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
              <path
                :class="{ hidden: !isOpen, 'inline-flex': isOpen }"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>

        <!-- Navbar items -->
        <div
          class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-between"
        >
          <div class="flex-shrink-0">
            <router-link
              to="/"
              class="text-white text-2xl font-bold"
              style="color: #08299b"
              >CareFinder</router-link
            >
          </div>
          <div class="hidden sm:block sm:ml-6">
            <div class="flex space-x-4 items-center justify-evenly">
              <router-link
                to="/"
                class="text-black px-3 py-2 rounded-md text-sm font-medium"
                >Home</router-link
              >
              <router-link
                to="/about"
                class="text-black px-3 py-2 rounded-md text-sm font-medium"
                >About</router-link
              >
              <router-link
                to="/findhospital"
                class="text-black px-3 py-2 rounded-md text-sm font-medium"
                >Find Hospital</router-link
              >
              <button
                @click="$router.push('/login')"
                style="background-color: #08299b"
                class="text-white px-3 py-2 rounded-md text-sm font-medium"
              >
                Login
              </button>
              <button
                @click="$router.push('/signup')"
                style="background-color: #08299b"
                class="text-white px-3 py-2 rounded-md text-sm font-medium"
              >
                Signup
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Mobile menu -->
    <div class="sm:hidden" :class="{ block: isOpen, hidden: !isOpen }">
      <div class="px-2 pt-2 pb-3">
        <router-link
          to="/"
          class="block px-3 py-2 rounded-md text-base font-medium"
          >Home</router-link
        >
        <router-link
          to="/about"
          class="block px-3 py-2 rounded-md text-base font-medium"
          >About</router-link
        >
        <router-link
          to="/findhospital"
          class="block px-3 py-2 rounded-md text-base font-medium"
          >Find Hospital</router-link
        >
        <button
          @click="$router.push('/login')"
          style="background-color: #08299b"
          class="block text-white px-3 py-2 rounded-md text-base font-medium"
        >
          Login
        </button>
        <button
          @click="$router.push('/signup')"
          style="background-color: #08299b"
          class="block text-white px-3 py-2 rounded-md text-base font-medium"
        >
          Signup
        </button>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { ref } from "vue";

export default defineComponent({
  setup() {
    const isOpen = ref(false);

    return {
      isOpen,
    };
  },
});
</script>
