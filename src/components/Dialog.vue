<template>
  <v-dialog v-model="show" max-width="500px">
    <v-card>
      <v-card-actions>
        <v-btn color="primary" flat @click.stop="show = false">Close</v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "Dialog",
  props: {
    val: Boolean,
  },
  computed: {
    show: {
      get() {
        return this.val;
      },
      set(val) {
        this.$emit("input", val);
      },
    },
  },
});
</script>