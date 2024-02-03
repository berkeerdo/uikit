<template>
  <div
    :class="{ dark: darkMode, 'bg-white': !darkMode, 'bg-gray-900': darkMode }"
    class="min-h-screen"
  >
    <Navbar :darkMode="darkMode" @toggle="toggleDarkMode" />
    <div class="container mx-auto p-4">
      <router-view />
    </div>
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
