<template>
  <nav
    :class="
      darkMode ? 'dark:bg-gray-800 bg-white shadow-lg' : 'bg-gray-200 shadow-lg'
    "
  >
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex items-center">
          <router-link
            to="/"
            :class="darkMode ? 'text-white' : 'text-black'"
            class="font-bold text-xl"
            >Home</router-link
          >
          <router-link
            to="/about"
            :class="darkMode ? 'text-white' : 'text-black'"
            class="ml-4 hover:text-white"
            >About</router-link
          >
          <router-link
            to="/contact"
            :class="darkMode ? 'text-white' : 'text-black'"
            class="ml-4 hover:text-white"
            >Contact</router-link
          >
        </div>
        <div>
          <button
            @click="$emit('toggle')"
            :class="darkMode ? 'text-white' : 'text-black'"
          >
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
  props: ["darkMode"],
};
</script>
