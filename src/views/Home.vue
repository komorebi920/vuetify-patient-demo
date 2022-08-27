<template>
  <v-app id="inspire" :style="{ background: $vuetify.theme.themes.dark.background }">
    <SideBar />
    <Navbar />
  </v-app>
</template>

<script>
import SideBar from "../components/SideBar.vue";
import Navbar from "../components/Navbar.vue";

export default {
  data: () => ({

  }),

  components: {
    SideBar,
    Navbar,
  },
};
</script>