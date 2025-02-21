<template>
  <nav class="bg-white shadow-md">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16 items-center">

        <div class="flex-shrink-0">
          <router-link to="/" class="text-2xl font-bold text-purple-600 hover:text-blue-600"
            >KeChaM Hub</router-link
          >
        </div>

        <div class="hidden md:flex space-x-4">
          <router-link
            to="/"
            class="text-gray-700 hover:text-blue-600"
            active-class="text-blue-600"
            exact
          >
            Home
          </router-link>
          <router-link
            to="/about"
            class="text-gray-700 hover:text-blue-600"
            active-class="text-blue-600"
          >
            About
          </router-link>
          <router-link
            to="/contact"
            class="text-gray-700 hover:text-blue-600"
            active-class="text-blue-600"
          >
            Contact
          </router-link>
          <router-link
            to="/apply"
            class="text-gray-700 hover:text-blue-600"
            active-class="text-blue-600"
          >
            Apply Now
          </router-link>
        </div>

        <div class="md:hidden">
          <button
            @click="toggleMenu"
            class="text-gray-700 hover:text-blue-600 focus:outline-none"
          >
            <svg
              v-if="!isMenuOpen"
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
            <svg
              v-else
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Dropdown for mobile menu -->
    <div
      v-if="isMenuOpen"
      class="md:hidden bg-gray-50 border-t border-gray-200"
    >
      <router-link
        to="/"
        class="block px-4 py-2 text-gray-700 hover:bg-gray-100"
        active-class="bg-blue-100"
        exact
      >
        Home
      </router-link>
      <router-link
        to="/about"
        class="block px-4 py-2 text-gray-700 hover:bg-gray-100"
        active-class="bg-blue-100"
      >
        About
      </router-link>
      <router-link
        to="/contact"
        class="block px-4 py-2 text-gray-700 hover:bg-gray-100"
        active-class="bg-blue-100"
      >
        Contact
      </router-link>
      <router-link
        to="/apply"
        class="block px-4 py-2 text-gray-700 hover:bg-gray-100"
        active-class="bg-blue-100"
      >
        Apply Now
      </router-link>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

<style scoped></style>
