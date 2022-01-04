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
import {Emit, Prop, Component, Vue } from "vue-property-decorator";

@Component({

})
export default class Dialog extends Vue {
    @Prop() public value!:Boolean;

    get show(){
        return this.value;
    }
}

</script>