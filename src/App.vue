<template>
  <div style="display: flex">
    <div>
      <Sidebar />
    </div>
    <div class="main-content">
      <v-btn @click="addCard()"> add </v-btn>
      <v-btn color="accent" large @click.stop="showScheduleForm = true"></v-btn>
      <Dialog :visible="showScheduleForm" @close="showScheduleForm = false" />

      <div class="content">
        <v-card class="card" v-for="item in items" :key="item">1</v-card>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Sidebar from "@/components/Sidebar.vue";
import Dialog from "@/components/Dialog.vue";

export default Vue.extend({
  name: "App",
  components: { Sidebar, Dialog },
  data() {
    return {
      items: 0,
      showScheduleForm: false,
    };
  },
  methods: {
    addCard() {
      this.items += 1;
    },
  },
});
</script>

<style scoped>
.sidebar {
  height: 100vh;
}

.main-content {
  padding: 10px;
  border: 1px solid rgb(99, 99, 99);
  width: 100%;
  height: 100vh;
  background: rgb(189, 189, 189);
}

.card {
  width: 70px;
  height: 70px;
  padding: 15px;
  margin: 10px;
}

.content {
  display: flex;
  flex-wrap: wrap;
}
</style>
