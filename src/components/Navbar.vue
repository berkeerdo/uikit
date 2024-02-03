<template>
  <nav class="dark:bg-gray-900 bg-gray-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex items-center">
          <router-link
            to="/"
            class="dark:text-gray-200 text-white font-bold text-xl"
            >Home</router-link
          >
          <router-link
            to="/about"
            class="dark:text-gray-400 ml-4 text-gray-300 hover:text-white"
            >About</router-link
          >
          <router-link
            to="/contact"
            class="dark:text-gray-400 ml-4 text-gray-300 hover:text-white"
            >Contact</router-link
          >
        </div>
        <div>
          <button @click="toggleDarkMode" class="text-white">
            {{ darkMode ? "Light Mode" : "Dark Mode" }}
          </button>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      darkMode: false,
    };
  },
  inject: ["darkMode", "toggleDarkMode"],
};
</script>
