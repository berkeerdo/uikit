<template>
  <div
    :class="{ dark: darkMode, 'bg-white': !darkMode, 'bg-gray-900': darkMode }"
  >
    <Navbar />
    <router-view />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";

export default {
  data() {
    return {
      darkMode: false,
    };
  },
  components: {
    Navbar,
  },
  provide() {
    return {
      darkMode: this.darkMode,
      toggleDarkMode: this.toggleDarkMode,
    };
  },
  methods: {
    toggleDarkMode() {
      this.darkMode = !this.darkMode;
      if (this.darkMode) {
        document.documentElement.classList.add("dark");
      } else {
        document.documentElement.classList.remove("dark");
      }
    },
  },
};
</script>
