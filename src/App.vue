<template>
  <v-app class="">
    <Sidebar />
  </v-app>
</template>

<script lang="ts">
import Vue from "vue";
import Sidebar from "@components/Sidebar.vue";

export default Vue.extend({
  name: "App",
  components: { Sidebar },
  data() {
    return {};
  },
});
</script>

<style scoped>
.sidebar {
  height: 100vh;
}
</style>
